pipeline {
  agent any
  stages {
    stage('Clonage du Depot') {
      steps {
        git(branch: 'main', url: 'https://github.com/GithubAnonyme/docker-node-example.git')
      }
    }

    stage('Construction de l\'Image Docker') {
      steps {
        script {
          dir('docker-node-example') {
            sh 'docker build -t image_test .'
          }
        }

      }
    }

  }
}