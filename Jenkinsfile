pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        sh 'mkdir -p /var/www/html'
        sh 'cp -r Jenkinsfile README.md index.html /var/www/html/'
      }
    }
  }
}
