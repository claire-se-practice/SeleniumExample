pipeline {
    agent {
        label "aws_jenkins"
    }

    stages {
        stage('git') {
            steps {
                git credentialsId: 'getaccount', url: 'https://github.com/claire-se-practice/SeleniumExample.git'
            }
        }
        stage('maven'){
          steps {
                sh 'mvn -Dmaven.test.failure.ignore=true clean test'
          }
        }
    }
