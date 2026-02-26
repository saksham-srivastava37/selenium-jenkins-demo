pipeline {
    agent any
    
    tools {
        maven 'Maven3'
        jdk 'JDK11'
    }

    stages {

        stage('Build and Run Tests') {
            steps {
               bat 'mvn clean test'
            }
        }

        stage('Publish Report') {
            steps {
                junit 'target/surefire-reports/*.xml'
            }
        }
    }
}
