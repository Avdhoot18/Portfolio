pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Avdhoot18/Portfolio.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No build required for static site'
            }
        }

        stage('Deploy') {
            steps {
                sh 'rm -rf /var/www/html/*'
                sh 'cp -r * /var/www/html/'
            }
        }
    }
}
