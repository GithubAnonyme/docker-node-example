pipeline {
  agent any
  stages {
    stage('Clone Repository') {
      steps {
        git 'https://github.com/votre-username/votre-repo.git'
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