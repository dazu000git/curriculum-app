pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/dazu000git/curriculum-app', branch: 'dev')
      }
    }
  stage('Log') {
      steps {
        sh 'ls -la'
      }
  }
    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile -t fuze365/curriculum-front:latest .'
      }
    }
  }
}
