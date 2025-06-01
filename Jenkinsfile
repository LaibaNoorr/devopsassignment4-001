stage('Deploy') {
    steps {
        sh '''
          echo Deploying application...
          mkdir -p /var/www/html
          cp -r Jenkinsfile README.md index.html /var/www/html/
        '''
    }
}

