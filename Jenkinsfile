pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "/path/to/code"
        TESTING_ENVIRONMENT = "testing-environment"
        PRODUCTION_ENVIRONMENT = "Mohitpreet Singh"
    }
    
    stages {
        stage('Build') {
            steps {
                
                echo "Fetching the source code from the directory path: ${env.DIRECTORY_PATH}"
                echo "Compiling the code and generating artifacts"
                
            }
        }
        
        stage('Test') {
            steps {
                echo "Running unit tests"
                echo "Running integration tests"
            }
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying the application to ${env.TESTING_ENVIRONMENT} environment"
            }
        }
        
        stage('Approval') {
            steps {
                echo "Waiting for manual approval..."
                sleep(time: 10, unit: 'SECONDS')
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to ${env.PRODUCTION_ENVIRONMENT} environment"
            }
        }
    }
}
