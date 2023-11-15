pipeline {
  agent any
  stages {
    stage('Cloner le depot') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/GithubAnonyme/docker-node-example.git']]])
      }
    }

    stage('Construire l\'image Docker') {
      steps {
        script {
          docker.build('https://github.com/GithubAnonyme/docker-node-example/Dockfile')
        }

      }
    }

  }
}