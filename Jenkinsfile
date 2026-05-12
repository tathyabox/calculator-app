pipeline {

    agent any

    environment {
        IMAGE_NAME = "192.168.137.51:5000/calculator-app:v1"
    }

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning repository'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push $IMAGE_NAME'
            }
        }

    }
}
