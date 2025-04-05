pipeline {
    agent {
        docker {
            image 'python:3.8'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building inside Docker container...'
                sh 'python --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "No tests yet!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo "Deployment simulation complete."'
            }
        }
    }
}
