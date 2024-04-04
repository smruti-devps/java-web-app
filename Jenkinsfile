pipeline {
    agent {
        node {
            label 'jenkins-slave-node-1-label'
        }
    }
    stages {
        stage('checkout code') {
            steps {
                git branch:'main', url: 'https://github.com/smruti-devps/java-web-app.git'

            }
        }
       stage('build code') {
           steps {
               sh '/opt/maven/bin/mvn clean package'
           }
       }  
    }
}