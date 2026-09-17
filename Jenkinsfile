pipeline {
    agent any
    tools {
        maven 'Maven'
    }

    stages{

        stage('Checkout'){
            steps{
                checkout scm
            }
        }

        stage('Build') {
            steps{
                echo 'Building the Application Code by Param'
                sh "mvn install"
            }
        }

        stage('Test') {
            steps{
                echo 'Testing the Project new'
                
            }
        }

        stage('Deploy') {
            steps{
                echo 'the Project is getting deployed'     
                sh "sudo cp "
                                     
            }
        }
    }

}
