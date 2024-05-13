pipeline {
    agent { label 'Jenkins-Agent' }
    tools {
        jdk 'java17'
        maven 'maven3'
    }
   
    stages{
        stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
        }

        stage("Checkout from SCM"){
                steps {
                    git branch: 'main', credentialsId: 'git', url: 'https://github.com/Deepajagadish/registration-app'
                }
        }

        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

       }

       
    }
}

