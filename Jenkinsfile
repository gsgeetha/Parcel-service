pipeline {
  agent slave1
  stages {
    stage('Checkout') {
      steps {
        sh 'rm -rf *'
        sh 'git clone https://github.com/gsgeetha/Parcel-service.git'
        sh 'cd Parcel-service'
        sh 'git checkout feature-1'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}
