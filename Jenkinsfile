pipeline
{
agent any
stages
{
 stage('scm checkout') {
            steps {
            git 'https://github.com/hardik-905/maven-project.git'  
            }
        }
stage('code compile')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true)  {
    sh 'mvn compile'
 } }}
}
}
