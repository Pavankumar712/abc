pipeline {
    agent any

    stages {
        stage('continonus download') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATC.git'
            }
        }
         stage('continonus build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continonus deploy') {
            steps {
                sh 'sshpass -p "pavan" scp target/DemoATR.war pavan@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
    }


