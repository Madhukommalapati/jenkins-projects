pipeline {
    agent any

    tools {
        jdk 'Java 17'
    }

    environment {
        ENV = 'hello welcome'
    }

    stages {
        stage('Practice') {
            steps {
                echo 'Practicing the declarative scripting'
            }
        }

        stage('Parallel Tests') {
            parallel {
                stage('T1') {
                    steps {
                        echo 'running test1'
                    }
                }
                stage('T2') {
                    steps {
                        echo 'running test2'
                    }
                }
            }
        }

        stage('Environment Echo') {
            steps {
                echo "${ENV} to Jenkins"
            }
        }

        stage('Manual Approval') {
            steps {
                input message: 'Is it successful?', ok: 'Yes'
            }
        }
    }

    post {
        success {
            echo 'Pipeline success'
        }
        failure {
            echo 'Something is wrong'
        }
        always {
            echo 'Make sure it works properly'
        }
    }
}
