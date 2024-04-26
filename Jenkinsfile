pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "F:\Deakin Masters Studies\2nd Sem\profe\Jenkinsfile"
        TESTING_ENVIRONMENT = "testing"
        PRODUCTION_ENVIRONMENT = "Continuous-Delivery-Pipeline"
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Fetching the source code from ${env.DIRECTORY_PATH}"
                echo "Compiling the code and generating necessary artifacts"
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
                echo "Deploying the application to a testing environment specified by ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                script {
                    echo "Waiting for manual approval..."
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to the production environment ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
