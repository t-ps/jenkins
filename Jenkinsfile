pipeline {
    agent any
    parameters {
        string(defaultValue: 'TEST', description: 'Parameter from JenkinsFike', name: 'HH_ENV' )
        choice(choices: 'USA\nCANDA\n', description: 'Parameter from jenkinsfile', name: 'region' )
    }

    stages {
        stage("prepare") {
            steps {
                script {
                    def param1 = "${params.PARAM1}"
                    //generate variables based on paramaters
                    // variables will be pased when running jobs
                    echo "Before SWITCH"
                    cos = param1 as int
                    echo "SWITCH CASE 1"
                    def machine01 = "${params.MACHINE1}"
                    MACHINE01 = machine01.split(',')
                    MACHINE01_P1 = "${MACHINE01[0]}"
                    MACHINE01_CPU = "${MACHINE01[1]}"
                    MACHINE01_RAM = "${MACHINE01[2]}"
                    MACHINE01_NET1 = "${MACHINE01[3]}"
                    MACHINE01_NET2 = "${MACHINE01[4]}"
                    MACHINE01_NET3 = "${MACHINE01[5]}"
                    MACHINE01_NET4 = "${MACHINE01[6]}"
                    env.PARAM1 = "${params.PARAM1}"
                    NET_P = ""
                    if (MACHINE01_NET1 == 'true') {
                        echo "This is inside \"SCRIPT\" "
                        NET_P = 'bridge '
                    }
                    if (MACHINE01_NET2 == 'true') {
                        NET_P += 'Isolated1 '
                    }
                    if (MACHINE01_NET3 == 'true') {
                        NET_P += 'Isolated2 '
                    }
                    if (MACHINE01_NET4 == 'true') {
                        NET_P += 'Isolated3'
                    }

                }
                build job: '../DevOPS/HelloWorld'
                echo "Steps in prepare"
                echo "${NET_P}"
                sh 'uptime'
                sh 'who'
            }
        }
        //echo "START OK START "
        stage("create_LVM") {
            //environment {
            //   Logical_Volume_Name = "${MACHINE01_P1}"
            //    Volume_Group = "kvm-vms"
            //}
            steps {
                echo "Creating LVM"
                script {
                    build job: '../VM_ACTIONS/VM_DeployLVM', parameters: [
                            string(name: 'Volume_Group', value: 'kvm-vms'),
                            string(name: 'Logical_Volume_Name', value: "${MACHINE01_P1}")]
                }
            }

        }

        stage('define_VM') {
            steps {
                build job: '../VM_ACTIONS/VM_DEFINE_VM', parameters: [
                        string(name: 'VM_NAME', value: "${MACHINE01_P1}"),
                        string(name: 'VM_CPU', value: "${MACHINE01_CPU}"),
                        string(name: 'VM_MEMORY', value: "${MACHINE01_RAM}"),
                        [$class: 'com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterValue', name: 'VM_NETWORK',
                         value: "${NET_P}"]]


            }
        }
        stage('deploy_VM_PXE'){
            steps {
                //build job: '../VM_ACTIONS/VM_DEPLOY_VM-PXE',
                //parameters: [string(name: 'VM_NAME', value: "${MACHINE01_P1}")]
                echo "NIBY DEPLOY_VM_PXE"
            }
        }

    }
}