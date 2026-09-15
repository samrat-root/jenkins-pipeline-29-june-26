pipeline {
    agent any

    stages{

        stage('checkout'){


        }

        stage('Build') {
            steps{
                echo 'Building the Application Code by Param'
            }
        }

        stage('Test') {
            steps{
                echo 'Testing the Project'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploying the Application '
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
