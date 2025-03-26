pipeline {
    agent any
    stages {
        stage('SCM checkout') {
            steps {
                git 'https://github.com/hardik-905/maven-project.git'
            }
        }
        stage('validate the code') {
            steps {
                withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true)  {
    sh 'mvn validate'
 }

            }
        }
        
    }
}
