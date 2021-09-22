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

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}
