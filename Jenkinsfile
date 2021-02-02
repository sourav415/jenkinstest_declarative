pipeline {
    agent any
    tools {
        maven 'maven-3.6.3' 
    }
    stages {
        stage('Build') {
            steps {
                echo 'Build my app'
               
            }
        }
        stage('Test') {
            
            when {
                expression{
                    env.BRANCH_NAME=='dev'
                       }
                 }
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
