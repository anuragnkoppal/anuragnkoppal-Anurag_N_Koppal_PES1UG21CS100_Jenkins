pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG21CS100-1 main.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG21CS100-1'
                echo 'Test Stage Successful'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn deploy'
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
