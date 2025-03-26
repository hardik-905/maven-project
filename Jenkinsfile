pipeline {
  agent any
  stages {
    stage('scm checkout') {
      steps {
        git 'https://github.com/hardik-905/maven-project.git'
      }
    }
    stage('print message') {
      steps {
       sh 'echo hello mumbai'
      }
    }
  }
}
