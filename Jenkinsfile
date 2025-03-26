pipeline {
  agent any
  stages {
    stage('scm checkout') {
      steps {
        git 'https://github.com/hardik-905/maven-project.git'
      }
    }
    stage('test the code') {
      steps {
      withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
        sh 'mvn test' 
        }

      }
    }
  } 
}
