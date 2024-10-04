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
        sh 'docker run -p 22:22 -d -v kali_home:/var/kali leplusorg/kali'
        sh 'docker ps'
      }
    }
  }
}
