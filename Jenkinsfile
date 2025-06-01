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
                echo "Deploying application..."
                # Example deploy commands below — customize to your app
                cp -r * /var/www/html/
                # sudo systemctl restart apache2 # If you use Apache, for example
                '''
            }
        }
    }
}
