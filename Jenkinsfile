pipeline {
    agent {
        AGENT-1
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 30, unit: 'MINUTES')
    }  
    environment {
                ENV_PIPE = 'pipeline Area'
            }
    stages {
        
        stage('Build') {
            
            steps {
                echo 'Building..'
                sh 'locatio is :$ENV_PIPE'
               
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }

    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success{
            echo 'I will run when success'
        }
        failure{
            echo 'I will Run When failure'
        }
    }    
}
