pipeline {
    agent any
    tools {
        nodejs 'NodeJS_18' // Replace with your configured NodeJS tool name
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'your_git_repo_url', branch: 'main' // Replace with your repository URL and branch
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build -- --configuration production'
            }
        }
        // stage('Deploy') {
        //   steps {
        //     // Add your deployment steps here, e.g. deploy to AWS S3, Google Cloud Storage etc.
        //     // Example:
        //     // sh 'aws s3 sync dist/your-app s3://your-s3-bucket'
        //     }
        // }
    }
}
