pipeline {
    agent any
    stages {
        stage("prepare") {
            steps {
                echo "HI This is simple, let's build some stuff"
                echo "Ha"
                echo "dwa"
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