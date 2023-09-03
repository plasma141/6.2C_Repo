pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "/path/to/code"
        TESTING_ENVIRONMENT = "testing-environment"
        PRODUCTION_ENVIRONMENT = "Mohitpreet Singh"
    }
    tools {
        maven 'Maven' 
        
    }
    stages {
        stage('Build') {
            steps {
                echo "Fetching the source code from the directory path: ${env.DIRECTORY_PATH}"
                echo "Compiling the code and generating artifacts"
                
            //   dir('DIRECTORY_PATH') {
                   
                     // sh 'mvn spotless:apply'
                     // sh 'mvn -Drat.ignoreErrors=true package'
                    // sh 'mvn -Drat.skip=true package'
                     //sh 'mvn clean package'
                    
                    
            //         }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests"
                
                //  dir('DIRECTORY_PATH') {
                //   sh 'mvn -Drat.skip=true test'
                    //sh 'mvn test'  // Using Maven for running tests
                
                    echo "Running integration tests"
                    //sh './run_integration_tests.sh'  // Replace with your integration test script
                    
                    
                    //}
                
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo "Checking the quality of the code"
                
            }
        }
        
        stage('Security Scan') {
            steps {
                echo "Scanning the code for security vulnerabilities"
                  // Using OWASP ZAP for security scan
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo "Deploying the application to ${env.TESTING_ENVIRONMENT} environment"
                  
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on the staging environment"
                
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to ${env.PRODUCTION_ENVIRONMENT} environment"
                
            }
        }
        
        stage('Email Notifications'){
            mail bcc: '', body: 'Jenkins Email Alerts ', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'mohitaulakh19@gmail.com.com'
        }
    }
    
  
}
