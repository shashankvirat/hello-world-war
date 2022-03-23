pipeline {
    agent any
    stages {
        stage('checkout') { 
            steps {
              git clone https://github.com/shashankvirat/hello-world-war
            }
        }
stage('build') { 
            steps {
              mvn clean package
            }
        }        
    }
}
