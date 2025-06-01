pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/LaibaNoorr/devopsassignment4-001.git'
            }
        }

      stage('Deploy') {
    steps {
        sh '''
          echo Deploying application...
          mkdir -p /var/www/html
          cp -r Jenkinsfile README.md index.html /var/www/html/
        '''
    }
}

    }}
