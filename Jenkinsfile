pipeline {
    agent any
    stages {
        stage('Pull from Git') {
            steps {
                git url: 'https://github.com/amitjoshi1709/instagram-clone.git', branch: 'main'
            }
        }
        stage('Deploy to Apache') {
            steps {
                sh 'sudo cp index.html /var/www/html/'
                sh 'sudo cp style.css /var/www/html/'
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}
