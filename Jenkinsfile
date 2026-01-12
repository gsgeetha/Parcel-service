pipeline {
  agent { label 'java_node' }
  stages {
    stage('Checkout') {
      steps {
        sh 'rm -rf *'
        sh 'git clone https://github.com/gsgeetha/Parcel-service.git'
      }
    }
    stage('Build') {
      steps {
        sh 'cd Parcel-service'
        sh 'git checkout feature-1'
        sh 'mvn clean install'
      }
    }
  }
}
