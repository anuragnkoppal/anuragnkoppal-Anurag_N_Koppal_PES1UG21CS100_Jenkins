pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS100-1'
                sh 'g++ main.cpp -o output'
                
            }
        }
        stage('Test') {
            steps {
                sh './output'
                
            }

        }
        stage('Deploy') {
            steps {
                
               
                echo 'Deploy'djkf
                
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
