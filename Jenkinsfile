pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build my app'
               
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
           echo 'always execute..'
           sh 'mvn build'
        }
            
    }
    
}
