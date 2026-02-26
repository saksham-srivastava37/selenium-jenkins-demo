pipeline {
    agent any
    
    tools {
        maven 'Maven3'
        jdk 'JDK11'
    }

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean test'
            }
        }

        stage('Publish Report') {
            steps {
                junit 'target/surefire-reports/*.xml'
            }
        }
    }
}
