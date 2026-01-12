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
        sh '''
        
          cd Parcel-service
          git checkout feature-1
          mvn clean install
        '''
      }
    }
  }
}
