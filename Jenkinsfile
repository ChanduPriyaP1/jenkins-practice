pipeline {
    agent {
        AGENT-1
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'MINUTES')
    }  
    environment {
                ENV_PIPE = 'pipeline Area'
            }
    stages {
        environment {
                    ENV_STAGES = 'Stages Area'
            }
        stage('Build') {
            environment {
                    ENV_STAGE = 'Stage Area'
            }
            steps {
                environment {
                    ENV_STEP = 'Steps Area'
            }
                echo 'Building..'
                sh 'locatio is :$ENV_STAGE'
                sh 'locatio is :$ENV_STAGES'
                sh 'locatio is :$ENV_STEP'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'locatio is :$ENV_PIPE'

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