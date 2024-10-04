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
        //sh 'su -'
        //sh 'docker run -p 22:22 -d -v ansible_home:/var/ansible_home alpine/ansible'
        mkdir '/var/terraform_home/'
        sh 'docker run terraform_home:/var/terrafrom_home hashicorp/terraform:latest'
      }
    }
    stage('Logs') {
      steps {
        sh 'docker ps -a'
      }
    }
  }
}
