pipeline {
  agent any
  stages {
    stage('Clonage du D�p�t') {
      steps {
        git 'https://github.com/GithubAnonyme/docker-node-example.git'
      }
    }

    stage('Construction de l\'Image Docker') {
      steps {
        script {
          dir('docker-node-example') {
            sh 'docker build -t Dockerfile .'
          }
        }

      }
    }

  }
}