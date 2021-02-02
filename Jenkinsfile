pipeline {
    agent any
    tools {
        maven 'maven-3.6.3' 
    }
    parameters{
        
        choice(name:'VERSION', choices: ['1.1','1.2'], description: 'deploy to production' )
        booleanParam(name:'executetest', defaultValue: 'true', description: '' )
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
                    params.executetest
                       }
                 }
            steps {
                echo 'Testing..'
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "version name is ${params.VERSION}"
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
