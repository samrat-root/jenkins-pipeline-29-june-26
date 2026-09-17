pipeline {
    agent any
   

    stages{

        stage('Checkout'){
            steps{
                checkout scm
            }
        }

        stage('Build') {
            steps{
                echo 'Building the Application Code by Param'
            }
        }

        stage('Test') {
            steps{
                echo 'Testing the Project new'
                
            }
        }

        stage('Deploy') {
            steps{
                echo 'the Project was deployed with Approval'     
                                     
            }
        }
    }

}