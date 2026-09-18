pipeline {

    agent any

    tools {
        maven 'Maven'
    }

    environment {
        APP_NAME = 'hello-world-war'
        DEPLOY_DIR = '/var/lib/tomcat10/webapps'
    }

    stages {

        stage('Checkout') {
            steps {

                echo 'Downloading source code from GitHub'

                checkout scm

            }
        }


        stage('Compile') {
            steps {

                echo 'Compiling Application'
            }
        }

        stage('Unit Test') {
            steps {

                echo 'Running Tests'

            }
        }

        stage('Package') {
            steps {

                echo 'Creating WAR File'

            }
        }

        stage('Deploy To Tomcat') {
            steps {

                script{
                    def name = 'Param'
                    echo name

                }
            
            }
        }

        stage('Verify Deployment') {
            steps {

                echo 'Deployment Completed'
            }
        }
    }

    post {

        always {

            junit 'target/surefire-reports/*.xml'
            echo 'Pipeline Finished'

        }

        success {

            echo 'Application Successfully Built and Deployed'
        }

        failure {

            echo 'Build Failed'
        }
    }
}
