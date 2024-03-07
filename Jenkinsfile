pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS100-1'
                sh 'g++ main.cpp -o output'
                
            }
        }
        stagwe('Test') {
            steps {
                sh './output'
                
            }

        }
        stage('Deploy') {
            steps {
                
               
                echo 'Deploy'
                
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
