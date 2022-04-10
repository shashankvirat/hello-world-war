pipeline{
      agent { label 'java1' }
      stages{
      stage('check out'){
                  steps{
                  sh "rm -rf hello-world-war"
                  sh "git clone https://github.com/shashankvirat/hello-world-war"
                  }
                  }
      stage('build'){
      steps{
      sh "pwd"
      sh "ls"
      sh "cd hello-world-war"
      sh "docker build -t shashankvirat/file:1.0 ."
      }
      }
       stage('publish'){
                  steps{
                        sh "docker login -u shashankvirat -p Virat@123"
                        sh "docker push shashankvirat/file:1.0"
                  }
            }
            stage('deploy'){
                  agent { label 'java2' }
                  steps{
                        sh "docker login -u shashankvirat -p Virat@123"
                        sh "docker pull shashankvirat -p Virat@123"
                        //sh "docker rm -f trail1"
                        sh "docker run -d -p 8082:8080 --name trail1 shashankvirat/file:1.0"
                  }
            }
      }
      }
