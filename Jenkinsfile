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
sh 'cp target/hello-world.war tomcat/webapps/hello-world'
}
}
}
}
