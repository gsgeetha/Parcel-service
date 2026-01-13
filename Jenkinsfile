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
    stage('Run App') {
      steps {
        timeout(time: 1, unit: 'MINUTES') {
          sh '''
          pwd
          ls
            java -jar target/simple-parcel-service-app-1.0-SNAPSHOT.jar
          '''
        }
      }
    }
  }
}
