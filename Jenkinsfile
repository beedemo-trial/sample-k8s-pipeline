pipeline {
 agent {
   kubernetes {
    //cloud 'kubernetes'
    label 'mypod'
     yaml """
     apiVersion: v1
     kind: Pod
     spec:
      containers:
      - name: maven
      image: maven:3.3.9-jdk-8-alpine
      command: ['cat']
      tty: true
      """
   }
 }
  stages {
    stage('Maven in k8s') {
      steps {
        container('maven') {
          sh 'mvn -version'
        }
      }
    }
  }
}
