
@Library("shared") _  
pipeline {
    agent { label "vinod" }
    
    stages {
        stage("Greeting"){
           steps{
               script{
                    greet()
               }
           }
        }
        stage('Cloning') {
            steps {
                script{
                    cloneRepo("https://github.com/vikas809028/Jenkins-CI-CD-Deployment.git","main")
                }
            }
        }

        stage('Building') {
            steps {
                script{
                    buildImage("jenkins-test")
                }
            }
        }

        stage('Publish on DockerHub') {
            steps {
                script{
                    publishOnDockerbub("jenkins-test")
                }
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker compose down && docker compose up -d'
            }
        }
    }
}
