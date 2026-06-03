pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build Frontend') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Deploy to S3') {
            steps {
                bat 'aws s3 sync build s3://ephraimimmanuel --delete'
            }
        }
    }
}