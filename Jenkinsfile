pipeline {
    agent any
    stages {
            stages ('checkout code') {
                steps {
                    git branch: 'main' , url: 'https://github.com/smruti-devps/java-web-app.git'

                }
            }
            stage ('build code') {
                steps {
                    sh 'mvn clean package'
                }
            }
            stage ('deploy to tomcat') {
                steps {
                    deploy adapters:[tomcat9(url:'http://13.126.107.212:8080/", credentialsId:'tomcatCred') ], war:'**/*.war'
                }
        }   }
    }
}    