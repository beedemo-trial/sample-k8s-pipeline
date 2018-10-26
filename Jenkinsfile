pipeline {
  agent {
    kubernetes {
      label 'kubernetes'
      containerTemplate {
        name 'jdk7-maven3'
        image 'maven:3.5-jdk-7-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
    stage('Maven in k8s') {
        steps {
            container('jdk7-maven3') {
                sh 'mvn -version'
            }
        }
    }
  }
}
