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
        echo 'No build needed for static HTML project'
      }
    }

    stage('Test') {
      steps {
        echo 'No automated tests for this static project, skipping'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying to Azure VM...'
          sh '''
            ssh -o StrictHostKeyChecking=no azureuser@<your-public-ip> "
              sudo mkdir -p /var/www/html &&
              sudo chown -R azureuser:azureuser /var/www/html &&
              rm -rf /var/www/html/* &&
              exit"
            scp -o StrictHostKeyChecking=no index.html azureuser@<172.201.217.238 >:/var/www/html/
          '''
        }
      }
    }
  }
}
