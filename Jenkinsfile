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
  deploy adapters: [tomcat9(credentialsId: 'ebc5b21e-67b4-4f92-9246-ed481dab3ded', path: '', url: 'http://52.66.242.47:8082/')], contextPath: null, war: '**/*.war'
  
}
}
}
}
