pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                echo "HI This is simple, let's build some stuff"
            }
        stage('Build') {
            steps {
                echo "Here we are builing"
                echo "And here are linking"
                echo "And this is the end of building"
            }
        }
        }

    }
    post {
        always {
            echo "This is the END, no matter how previous stuff has ended :) "
        }
    }
}