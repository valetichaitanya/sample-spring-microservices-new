pipeline {
    agent any

   
    stages {
        stage('Build') {
            steps {
                
                sh """mvn --version \
                    cd config-service \
                    mvn package \
                    cd .."""
               

          
            }
        }
    }
}
