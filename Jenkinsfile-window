pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                git credentialsId: 'getaccount', poll: false, url: 'https://github.com/claire-se-practice/SeleniumExample.git'
            }
        }
        stage('maven'){
          steps {
                bat 'mvn clean test'
          }
        }
    }
}
