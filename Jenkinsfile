pipeline {
    agent any
    parameters {
        string(name: 'FINAL_VERSION', defaultValue: '1.1.2',description: 'Enter the Version Number: ')
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
