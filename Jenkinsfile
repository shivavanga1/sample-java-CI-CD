pipeline {
    agent any

    tools {
        maven "Maven" // Ensure this is the name configured in Jenkins
    }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean package' // Make sure pom.xml is in the root
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Deployment steps here
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
