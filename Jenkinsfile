pipeline {
    agent {
        label 'ec2'
    }

   
    stages {
        stage('Build') {
            steps {
                
                sh '''cd config-service \
                
                      mvn package \
                      
                      cd ..'''
               

          
            }
        }
    }
}
