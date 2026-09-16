pipeline {
    agent any
    environment {
        FINAL_VERSION = '1.2.3'
    }

    stages{

        stage('Checkout'){
            steps{
                checkout scm
            }
        }

        stage('Build') {
            when{
                expression{
                    BRANCH_NAME == 'param' || BRANCH_NAME == 'main'
                }
            }
            steps{
                echo 'Building the Application Code by Param'
            }
        }

        stage('Test') {
            steps{
                echo 'Testing the Project new'
                echo "The Testing Tool version will be ${FINAL_VERSION}"
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
