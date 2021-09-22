pipeline {
    agent any

   
    stages {
        stage('Build') {
            steps {
                

                // Run Maven 
                sh """mvn version\
                cd config-service\
                mvn package\
                cd .."""
                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
          

          
            }
        }
    }
}
