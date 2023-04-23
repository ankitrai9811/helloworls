pipeline {
agent any
stages {
stage('Build') {
steps {
  sh 'mvn clean package'
}
}
stage('Deploy') {
steps {
  deploy adapters: [tomcat9(credentialsId: 'ebc5b21e-67b4-4f92-9246-ed481dab3ded', path: '', url: 'http://65.0.183.76:8082/')], contextPath: null, war: '**/*.war'
  sh 'cp target/demo-0.0.1-SNAPSHOT.war tomcat/webapps/demo-0.0.1-SNAPSHOT.war'
}
}
}
}
