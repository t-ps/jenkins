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
                    def param1 = "${params.PARAM1}" as int
                    //generate variables based on paramaters
                    // variables will be pased when running jobs
                    echo "Before SWITCH"
                    
										echo "SWITCH CASE 1"
										if ( param1 == 1 ) {
										// Prepare parameters for machine1
			 								def machine01 = "${params.MACHINE1}"
		   		     	  	  MACHINE01 = machine01.split(',')
		   		            MACHINE01_P1 = "${MACHINE01[0]}"
		   		            MACHINE01_CPU = "${MACHINE01[1]}"
		   		            MACHINE01_RAM = "${MACHINE01[2]}"
		   		            MACHINE01_NET1 = "${MACHINE01[3]}"
		   		            MACHINE01_NET2 = "${MACHINE01[4]}"
		   		            MACHINE01_NET3 = "${MACHINE01[5]}"
		   		            MACHINE01_NET4 = "${MACHINE01[6]}"
		                  NET_01_P = ""
		                  if (MACHINE01_NET1 == 'true') {
		                      echo "This is inside \"SCRIPT\" "
		                      NET_01_P = 'bridge '
		                  }
		                  if (MACHINE01_NET2 == 'true') {
		                      NET_01_P += 'Isolated1 '
		                  }
		                  if (MACHINE01_NET3 == 'true') {
		                      NET_01_P += 'Isolated2 '
		                  }
		                  if (MACHINE01_NET4 == 'true') {
		                      NET_01_P += 'Isolated3'
		                  }
											// Setting up global variable
											env.NET_01_P = NET_01_P
											echo "INSIDE SWITCH CASE 1"
										}
										
										echo "SWITCH CASE 2"
										if ( param1 >= 2 ) {
										// Prepare parameters for machine2
											def machine02 = "${params.MACHINE2}"
		   		     	  	  MACHINE02 = machine03.split(',')
		   		            MACHINE02_P1 = "${MACHINE02[0]}"
		   		            MACHINE02_CPU = "${MACHINE02[1]}"
		   		            MACHINE02_RAM = "${MACHINE02[2]}"
		   		            MACHINE02_NET1 = "${MACHINE02[3]}"
		   		            MACHINE02_NET2 = "${MACHINE02[4]}"
		   		            MACHINE02_NET3 = "${MACHINE02[5]}"
		   		            MACHINE02_NET4 = "${MACHINE02[6]}"
		                  NET_02_P = ""
		                  if (MACHINE02_NET1 == 'true') {
		                      echo "This is inside \"SCRIPT\" "
		                      NET_02_P = 'bridge '
		                  }
		                  if (MACHINE02_NET2 == 'true') {
		                      NET_02_P += 'Isolated1 '
		                  }
		                  if (MACHINE02_NET3 == 'true') {
		                      NET_02_P += 'Isolated2 '
		                  }
		                  if (MACHINE02_NET4 == 'true') {
		                      NET_02_P += 'Isolated3'
		                  }
											// Setting up global variable
											env.NET_02_P = NET_02_P

										} 

										echo "SWITCH CASE 3"
										if ( param1 >=3 ) {
											// Prepare parameters for machine3
											def machine03 = "${params.MACHINE3}"
		   		     	  	  MACHINE03 = machine03.split(',')
		   		            MACHINE03_P1 = "${MACHINE03[0]}"
		   		            MACHINE03_CPU = "${MACHINE03[1]}"
		   		            MACHINE03_RAM = "${MACHINE03[2]}"
		   		            MACHINE03_NET1 = "${MACHINE03[3]}"
		   		            MACHINE03_NET2 = "${MACHINE03[4]}"
		   		            MACHINE03_NET3 = "${MACHINE03[5]}"
		   		            MACHINE03_NET4 = "${MACHINE03[6]}"
		                  NET_03_P = ""
		                  if (MACHINE03_NET1 == 'true') {
		                      echo "This is inside \"SCRIPT\" "
		                      NET_03_P = 'bridge '
		                  }
		                  if (MACHINE03_NET2 == 'true') {
		                      NET_03_P += 'Isolated1 '
		                  }
		                  if (MACHINE03_NET3 == 'true') {
		                      NET_03_P += 'Isolated2 '
		                  }
		                  if (MACHINE03_NET4 == 'true') {
		                      NET_03_P += 'Isolated3'
		                  }
											// Setting up global variable
											env.NET_03_P = NET_03_P

										}
										echo "SWITCH CASE 4"
										if ( param1 >=4 ) {
											// Prepare parameters for machine4
											def machine04 = "${params.MACHINE4}"
		   		     	  	  MACHINE04 = machine04.split(',')
		   		            MACHINE04_P1 = "${MACHINE04[0]}"
		   		            MACHINE04_CPU = "${MACHINE04[1]}"
		   		            MACHINE04_RAM = "${MACHINE04[2]}"
		   		            MACHINE04_NET1 = "${MACHINE04[3]}"
		   		            MACHINE04_NET2 = "${MACHINE04[4]}"
		   		            MACHINE04_NET3 = "${MACHINE04[5]}"
		   		            MACHINE04_NET4 = "${MACHINE04[6]}"
		                  NET_04_P = ""
		                  if (MACHINE04_NET1 == 'true') {
		                      echo "This is inside \"SCRIPT\" "
		                      NET_04_P = 'bridge '
		                  }
		                  if (MACHINE04_NET2 == 'true') {
		                      NET_04_P += 'Isolated1 '
		                  }
		                  if (MACHINE04_NET3 == 'true') {
		                      NET_04_P += 'Isolated2 '
		                  }
		                  if (MACHINE04_NET4 == 'true') {
		                      NET_04_P += 'Isolated3'
		                  }

											// Setting up global variable
											env.NET_04_P = NET_04_P
	
										}
										echo "SWITCH CASE 5"
										if ( param1 >=5 ) {
											// Prepare parameters for machine5
											def machine05 = "${params.MACHINE4}"
		   		     	  	  MACHINE05 = machine05.split(',')
		   		            MACHINE05_P1 = "${MACHINE05[0]}"
		   		            MACHINE05_CPU = "${MACHINE05[1]}"
		   		            MACHINE05_RAM = "${MACHINE05[2]}"
		   		            MACHINE05_NET1 = "${MACHINE05[3]}"
		   		            MACHINE05_NET2 = "${MACHINE05[4]}"
		   		            MACHINE05_NET3 = "${MACHINE05[5]}"
		   		            MACHINE05_NET4 = "${MACHINE05[6]}"
		                  NET_05_P = ""
		                  if (MACHINE05_NET1 == 'true') {
		                      echo "This is inside \"SCRIPT\" "
		                      NET_05_P = 'bridge '
		                  }
		                  if (MACHINE05_NET2 == 'true') {
		                      NET_05_P += 'Isolated1 '
		                  }
		                  if (MACHINE05_NET3 == 'true') {
		                      NET_05_P += 'Isolated2 '
		                  }
		                  if (MACHINE05_NET4 == 'true') {
		                      NET_05_P += 'Isolated3'
		                  }
											// Setting up global variable
											env.NET_05_P = NET_05_P
										}
										echo "SWITCH CASE 6"
										if ( param1 >=6 ) {
											// Prepare parameters for machine6
											def machine06 = "${params.MACHINE6}"
		   		     	  	  MACHINE06 = machine06.split(',')
		   		            MACHINE06_P1 = "${MACHINE06[0]}"
		   		            MACHINE06_CPU = "${MACHINE06[1]}"
		   		            MACHINE06_RAM = "${MACHINE06[2]}"
		   		            MACHINE06_NET1 = "${MACHINE06[3]}"
		   		            MACHINE06_NET2 = "${MACHINE06[4]}"
		   		            MACHINE06_NET3 = "${MACHINE06[5]}"
		   		            MACHINE06_NET4 = "${MACHINE06[6]}"
		                  NET_06_P = ""
		                  if (MACHINE06_NET1 == 'true') {
		                      echo "This is inside \"SCRIPT\" "
		                      NET_06_P = 'bridge '
		                  }
		                  if (MACHINE06_NET2 == 'true') {
		                      NET_06_P += 'Isolated1 '
		                  }
		                  if (MACHINE06_NET3 == 'true') {
		                      NET_06_P += 'Isolated2 '
		                  }
		                  if (MACHINE06_NET4 == 'true') {
		                      NET_06_P += 'Isolated3'
			                }
											// Setting up global variable
											env.NET_06_P = NET_06_P
										}
										
									echo "PREPARED ${param1} MACHINES FOR DEPLOYMENT"
									for (int x=1; x<=param1;x++) {
											echo "Machine ${x} is ${MACHINE0${x}_P1}
									}
                }
                build job: '../DevOPS/HelloWorld'
                echo "Steps in prepare"
								echo "MACHINE 1 = ${MACHINE01_P1}"
								echo "MACHINE  = ${MACHINE01_P1}"
								echo "MACHINE 1 = ${MACHINE01_P1}"
								echo "MACHINE 1 = ${MACHINE01_P1}"
								echo "MACHINE 1 = ${MACHINE01_P1}"
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
                         value: "${env.NET_01_P}"]]


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
