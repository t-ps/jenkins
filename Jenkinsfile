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
                    def machine01 = "${params.MACHINE1}"
                    MACHINE01 = machine01.split(',')
                    MACHINE01_P1 = "${MACHINE01[0]}"
                    MACHINE01_P2 = "${MACHINE01[1]}"
                    MACHINE01_P3 = "${MACHINE01[2]}"
                    MACHINE01_P4 = "${MACHINE01[3]}"
                    MACHINE01_P5 = "${MACHINE01[4]}"
                    MACHINE01_P6 = "${MACHINE01[5]}"
                    MACHINE01_P7 = "${MACHINE01[6]}"
                    env.PARAM1 = "${params.PARAM1}"
                    if (true) {
                        echo "This is inside \"SCRIPT\" "    
                    
                    }
                }
                echo "Steps in prepare"
                sh 'uptime'
            }
        }
                //echo "START OK START "
        stage("create_LVM") {
             environment {
                    Logical_Volume_Name = "${MACHINE01_P1}"
                    Volume_Group = "kvm-vms"
                }
            steps {
                echo "Creating LVM"
                //sh 'echo \"/export/shares/jenkins/scripts/VM_DeployLVM.bsh ${MACHINE01[1]} kvm-vms\"'
                sh 'echo Cos ${Logical_Volume_Name} ${Volume_Group}}'
                echo "Fparam0=${MACHINE01[0]}"
                echo "Fparam1=${MACHINE01[1]}"
                echo "Fparam2=${MACHINE01[2]}"
            }
                      
        }
            
        stage('Build') {
            steps {
                sh 'uname -a'

            }
        }

    }
}
