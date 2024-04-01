pipeline {
    agent any

    environment {
        // Define environment variables if needed
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/MuhammadTaimoorAnwar511/lab10'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    dir('app') {
                        sh 'npm install'
                    }
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    dir('app') {
                        sh 'npm run build'
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    dir('app') {
                        // Replace with actual test command
                        sh 'npm test'
                    }
                }
            }
        }

        stage('Dockerize and Deploy') {
            steps {
                script {
                    // Assuming the Dockerfile is at the root or specify the path
                    sh 'docker build -t express-mongodb-app .'
                    // Assuming docker-compose.yml is properly set up in the project root
                    sh 'docker-compose up -d'
                }
            }
        }
    }
}

