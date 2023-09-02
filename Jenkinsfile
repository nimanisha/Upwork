pipeline {
    agent none
    stages {
        stage('Git Checkout') {
            agent any
/*            tools {

            }
            options {
                // Timeout counter starts BEFORE agent is allocated
               // timeout(time: 1, unit: 'SECONDS')
*/            
            steps {
               git 
                git branch :'main',changelog: flase ,credentialsId: '91a75276-ccff-4636-947d-940712d81400', url: 'https://github.com/nimanisha/Upwork.git'
            }
        }
                
        stage('COMPILE') {        
             steps {
               sh "npm install"
               sh "npm run lint"
               sh "npm run prettier"
            }
        }
        stage('Dependency Scan') {        
             steps {
              DependencyCheck additionalArguments:'',odcInstallation: 'DP-check'
                dependencyCheckPublisher pattern: '**/dependency-check-report.xml' 
                        }
        }
    }
}
