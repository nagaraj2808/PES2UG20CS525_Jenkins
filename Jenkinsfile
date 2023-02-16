pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('main/') {
                    sh 'g++ hello.cpp'
                }
                build job: 'PES2UG20CS525-1'
            }
        }

        stage('Test') {
            steps {
               dir('main/') {
                    sh 'g++ hello.cpp'
                }
                echo "Build stage successful"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployment successfull"
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
