pipeline {
  agent {
    label 'java-maven'
  }
  stages {
    stage('Maven in k8s') {
        steps {
            container('global-maven3-jdk8') {
                sh 'mvn -version'
            }
        }
    }
  }
}
