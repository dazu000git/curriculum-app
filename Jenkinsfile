pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/faraday-academy/curriculum-app', branch: 'dev')
      }
    }
    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile -t fuze365/curriculum-front:latest .'
      }
    }
  }
}
