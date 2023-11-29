pipeline {
  agent {
    label {
      label "built-in"
    }
  }
  stages {

    stage ("1st") {
      steps {
        sh "yum install httpd -y"
      }
    }

    stage ("2nd") {
      steps {
        
