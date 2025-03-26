pipeline {
    agent any
    stages {
        stage('SCM checkout') {
            steps {
                git 'https://github.com/hardik-905/maven-project.git'
            }
        }
        stage('Test message') {
            steps {
                sh 'echo hello mumbai'
            }
        }
        stage('message') {
            steps {
                sh 'echo delhi'
            }
        }
    }
}
