pipeline {
    agent any
    parameters {
        choice(name: 'FINAL_VERSION',choices: ['1.2.3','1.3.2','1.4.2'] ,description: 'Enter the Version Number: ')
        booleanParam(name: 'Test-Approval', defaultValue: false, description: 'Approval')
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
            }
        }

        stage('Test') {
            steps{
                echo 'Testing the Project new'
                echo "The Testing Tool version will be ${params.FINAL_VERSION}"
            }
        }

        stage('Deploy') {
            when {
                expression{
<<<<<<< HEAD
                    params['Test-Approval'] == true
=======
                    params['Test-Approval'] = true
>>>>>>> 85655b2ab9c48cfc18a0feae52f20a13cc645c8c
                }
            }
            steps{
                echo 'the Project was deployed with Approval'
            }
            steps{
                echo 'Deploying the Application '
                withCredentials([
                    usernamePassword(credentialsId: 'demo-server-credentials', usernameVariable: 'USER', passwordVariable: 'PWD')
               ]) {
                    echo "The Credentials are: ${USER} and ${PWD}"
                    }       
                                     
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