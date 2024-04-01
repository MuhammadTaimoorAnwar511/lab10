pipeline {

    agent any

    
    stages {
         stage('build') {
          steps {
              sh 'npm install'
            }
          }
        
        stage('Docker Comopse Up') {
            steps {
               
                    sh "echo-docker-compose-up"
                
            }
        }
         stage('kill') {
            steps {
               
                    sh "echo-docker-compose-down"
                
            }
        }
    }
}
