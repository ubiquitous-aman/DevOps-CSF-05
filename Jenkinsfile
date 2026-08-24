pipeline {
    agent any

    environment {
        PATH = "C:\\Program Files\\nodejs;${env.PATH}"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                echo 'Installing backend dependencies...'
                bat 'cd backend && npm install'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                bat 'cd backend && npm test'
            }
        }
    }

    post {
        success {
            echo '✅ BUILD SUCCESSFUL'
        }

        failure {
            echo '❌ BUILD FAILED'
        }
    }
}