pipeline {
    agent any
    options {
        timeout(time: 30, unit: 'MINUTES') 
        disableConcurrentBuilds()
        
    }
   
     environment {
        ENV = 'Pipe level variable'
            }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'echo "$ENV"'
            }
        }
        stage('Deploy') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
            }
            steps {
                echo 'Deploying....'
            }
        }
        
    }
    
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}