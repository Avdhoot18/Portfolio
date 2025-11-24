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

// pipeline {
//     agent any

//     environment {
//         DEPLOY_DIR = 'C:\\inetpub\\wwwroot' // IIS web root folder
//     }

//     stages {
//         stage('Checkout') {
//             steps {
//                 echo 'Cloning project from GitHub...'
//                 git branch: 'main', url: 'https://github.com/Avdhoot18/Portfolio.git'
//             }
//         }

//         stage('Build') {
//             steps {
//                 echo 'Build Step: Check files in workspace'
//                 bat 'dir'
//             }
//         }

//         stage('Deploy') {
//             steps {
//                 echo "Deploying site to IIS folder..."
//                 bat """
//                     if not exist ${DEPLOY_DIR} mkdir ${DEPLOY_DIR}
//                     copy /Y index.html ${DEPLOY_DIR}\\
//                 """
//             }
//         }

//         stage('Access Link') {
//             steps {
//                 echo '✅ Deployment done!'
//                 echo '👉 Access your page here: http://localhost/index.html'
//             }
//         }
//     }
// }
