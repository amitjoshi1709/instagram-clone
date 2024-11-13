pipeline {
    agent any
    stages {
        stage('Pull from GitHub') {
            steps {
                git url: 'https://github.com/amitjoshi1709/instagram-clone.git', branch: 'main'
            }
        }
        stage('Deploy to Web Server') {
            steps {
                sh 'sudo cp index.html /var/www/html/'
                sh 'sudo cp style.css /var/www/html/'
            }
        }
        stage('Restart Web Server') {
            steps {
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}
