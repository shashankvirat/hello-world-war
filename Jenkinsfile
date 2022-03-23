pipeline {
    agent { label 'java' }
    stages {
        stage('checkout') { 
            steps {
              sh "git clone https://github.com/shashankvirat/hello-world-war"
            }
        }
stage('build') { 
            steps {
              sh "mvn clean package"                
            }
        }        
    stage('Deploy') { 
            steps {
              sh " cp /home/slave2/jenkins/workspace/job1/target/hello-world-war-1.0.0 /opt/apache-tomcat-9.0.60/webapps"   
}
    }
    }
    }
