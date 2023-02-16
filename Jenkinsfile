pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('main/') {
                    sh 'g++ hello.cpp'
                }
                build job: 'my-other-job'
            }
        }

        stage('Test') {
            steps {
                sh './a.out'
                echo "Build stage successful"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployment stage"
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
