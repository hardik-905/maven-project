pipeline {
  agent any
  stages {
    stage('scm checkout') {
      steps {
        git 'https://github.com/hardik-905/maven-project.git'
      }
    }
    stage('package the code') {
      steps {
      withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
        sh 'mvn clean package' 
        }

      }
    }
    stage('deploy the code on tomcat') {
      steps {
      sshagent(['JenkinsCICD']) {
      sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Jenkins_maven/webapp/target/webapp.war ec2-user@172.31.1.144:/usr/share/tomcat/webapps'

      }

      }
    }
  } 
}
