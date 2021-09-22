pipeline {
    agent any

   
    stages {
        stage('Build') {
            steps {
                
                sh '''cd config-service 
                      mvn package
                      cd ..'''
               

          
            }
        }
    }
}
