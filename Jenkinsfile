pipeline {
    agent any
    stages {
        stage ('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/smruti-devps/java-web-app.git'
            }
            
        }
        stage ('buildcode code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }

        }
        stage ('deploy to tomcat') {
            steps {
                deploy adapters:[tomcat9(url:'http://13.233.59.88:8080/', credentialsId:'tomcatcred')], war:'**/*.war'
            }

        }
    }
}