pipeline {
    agent any

    tools {
        maven "Maven" // Ensure this matches the name configured in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean package' // Builds the project and creates a JAR file
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test' // Executes tests
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Here you can add deployment scripts or commands, e.g., copying to a server
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
