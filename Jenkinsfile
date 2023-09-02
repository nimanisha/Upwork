pipeline {
    agent none
    stages {
      /*  stage('Git Checkout') {
            agent any
            tools {

            }
            options {
                // Timeout counter starts BEFORE agent is allocated
               // timeout(time: 1, unit: 'SECONDS')
            }
            steps {
                git branch :'main',changelog: flase ,credentialsId:
            }
        }
         stage('COMPILE') {        
             steps {
                git branch :'main',changelog: flase ,credentialsId:
            }
   */     
        stage('Dependency Scan') {        
             steps {
              DependencyCheck additionalArguments:'',odcInstallation: 'DP-check'
                dependencyCheckPublisher pattern: '**/dependency-check-report.xml' 
                        }
        }
    }
}
