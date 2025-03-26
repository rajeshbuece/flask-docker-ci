pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/rajeshbuece/flask-docker-ci.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-docker-ci .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 flask-docker-ci'
            }
        }
    }
}

