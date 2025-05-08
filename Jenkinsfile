pipeline {
    agent any

    tools {
        // Define tools needed for the build
        jdk 'Java 7'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean install'  // Replace with your actual build command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'  // Replace with your test command
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Cleanup steps (if any)
        }
    }
}
