pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t whalerider02/hangman-app-mp:latest --platform linux/amd64,linux/arm64 .'
      }
    }

    stage('push') {
      steps {
        sh 'docker push whalerider02/hangman-app-mp:latest'
      }
    }

  }
}