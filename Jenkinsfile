pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository containing the Flask app
                git 'https://your-repository-url.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Build a Docker image for the Flask app
                    sh 'docker build -t flask-app .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // Run the Flask app in a Docker container
                    sh 'docker run -d -p 5000:5000 flask-app'
                }
            }
        }
    }

    post {
        always {
            // Clean up workspace after the pipeline
            cleanWs()
        }
    }
}
