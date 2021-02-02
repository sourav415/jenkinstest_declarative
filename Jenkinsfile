pipeline {
    agent any
    tools {
        maven 'apache-maven-3.6.3' 
    }
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
           sh 'mvn --version'
        }
            
    }
    
}
