pipeline {
    agent { label 'java' }
    stages {
        stage('checkout') { 
            steps {
              sh "rm -rf *"
              sh "git clone https://github.com/shashankvirat/hello-world-war"
            }
        }
stage('build') { 
            steps {
              sh "mvn clean package"
            }
        }        
    }
}