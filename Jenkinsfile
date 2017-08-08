pipeline {
    agent any
    stages {
        stage("prepare") {
            steps {
                script {
                    echo "Checking for  "
                    echo "Param1=${params.PARAM1}"
                    echo "Machine1=${params.MACHINE1}"
                    echo "Machine2=${params.MACHINE2}"
                    echo "Machine3=${params.MACHINE3}"
                    echo "Machine4=${params.MACHINE4}"
                    echo "Machine5=${params.MACHINE5}"

                    def reg_check = /(server[0-9]|desktop[0-9]),([1-4]{1}),(true|false),(true|false),(true|false),(true|false)/
                    def machine_find_params = ($ { params.MACHINE1 } =~ reg_check)
                    echo "dsds" + machine_find_params.count
                    echo machine_find_params[0][1]
                    echo machine_find_params[0][2]
                }

            }
        }
        stage("create_LVM"){
            steps {
                //build job: '../VM_ACTIONS/VM_DeployLVM',
                //parameters: [string(name: 'Volume_Group', value: 'kvm-vms'),
                //             string(name: 'Logical_Volume_Name', value: "${MACHINE01_TYPE}")]
                echo "111"
            }

        }
        stage('Build') {
            steps {
                echo "Here we are builing"
                echo "And here are linking"
                echo "And this is the end of building"
                sh 'uptime'
                sh 'uname -a'

            }
        }

    }
    post {
        always {
            echo "This is the END, no matter how previous stuff has ended :) "
        }
    }

}
