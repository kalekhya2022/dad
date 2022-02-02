pipeline {
    agent any

    stages {
        stage('continous download') {
            steps {
                git 'https://github.com/kalekhya2022/DemoATR.git'
            }
        }
        stage('continous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continous deploy') {
            steps {
                sh 'sshpass -p "raghu" scp target/DemoATR.war raghu@172.17.0.4:/opt/apache-tomcat-9.0.58/webapps'
            }
        }
    }
}

