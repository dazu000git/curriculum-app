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
        sh 'su -'
        sh 'docker run -p 22:22 -d -v ansible_home:/var/ansible_home alpine/ansible'
        sh 'docker ps -a'
      }
    }
    stage('Logs') {
        sh 'docker logs'
    }
  }
}
