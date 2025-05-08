pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/kshitijgupta1603/helplink.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build App') {
            steps {
                bat 'npm run build'
            }
        }
    }

    post {
        success {
            echo 'Build successful. Files are in the dist/ directory.'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
