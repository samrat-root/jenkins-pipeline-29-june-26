pipeline {
    agent any

    stages{

        stage('Checkout'){
            steps{
                git 'https://github.com/samrat-root/jenkins-pipeline-29-june-26.git'
            }
        }

        stage('Build') {
            when{
                expression{
                    BRANCH_NAME == "main"
                }
            }
            steps{
                echo 'Building the Application Code by Param'
            }
        }

        stage('Test') {
            steps{
                echo 'Testing the project'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploying the Application '
                echo 'Building the Application Code in param branch'
            }
        }
    }

    post{
        always{
            echo 'This is always executed'
        }
        success{
            echo 'This indicates succesful execution of the pipeline'
        }
        failure{
            echo 'This indicates at least one failure in the pipeline'
        }

    }


}
