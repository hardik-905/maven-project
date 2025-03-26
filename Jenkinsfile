pipeline {
  agent any
  stages {
    stage('git SCM checkout')
    steps {
      git https://github.com/hardik-905/maven-project.git
    }

    stage('level 2')
    steps {
      sh 'echo mumbai'
    }

    stage('level3')
    steps {
      echo 'hello2'
    }

  }
}
  
