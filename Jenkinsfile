pipeline {
    agent any

    tools {
        // Define tools needed for the build
        jdk 'Java 17'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
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
