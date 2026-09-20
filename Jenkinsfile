pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }
pipeline {
    agent any

    stages {

        stage('Pull Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t docker-jenkins-demo:v1 .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f docker-jenkins-demo-container || true'
                sh 'docker run -d --name docker-jenkins-demo-container docker-jenkins-demo:v1'
            }
        }

        stage('Display Container') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
        stage('Test') {
            steps {
                echo 'Testing application...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }

    }
}
