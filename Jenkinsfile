node {
    stage('checkout code') {
        git branch:'main', url: 'https://github.com/smruti-devps/java-web-app.git'

    }
    stage('build code') {
        sh '/opt/maven/bin/mvn clean package'

    }
    stage('deploy to tomcat') {
        deploy adapters: [tomcat9(url:'http://43.204.37.42:8080/', credentialsId: 'tomcatcred')], war:'**/*.war'

    }
}