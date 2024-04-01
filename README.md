pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    sh 'docker build -t my-hello-world .'
                }
            }
        }
        stage('Push') {
            steps {
                script {
                    // Push Docker image (optional)
                    sh 'docker push my-hello-world'
                }
            }
        }
    }
}
