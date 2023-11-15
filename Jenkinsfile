pipeline {
  agent any
  stages {
    stage('Clone Repository') {
      steps {
        git 'https://github.com/GithubAnonyme/docker-node-example'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t monapp .'
      }
    }

    stage('Security Scan') {
      steps {
        sh 'trivy image monapp'
      }
    }

    stage('Run Tests') {
      steps {
        sh 'npm run test'
      }
    }

  }
}