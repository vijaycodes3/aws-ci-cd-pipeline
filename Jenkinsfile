pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/VijayAnanthula/aws-ci-cd-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t vijay-node-app .'
            }
        }
        stage('Push Image') {
            steps {
                sh 'echo "Pushing Docker image to DockerHub..."'
                sh 'docker tag vijay-node-app vijayananthula/vijay-node-app:latest'
                sh 'docker push vijayananthula/vijay-node-app:latest'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/deployment.yaml'
                sh 'kubectl apply -f k8s/service.yaml'
            }
        }
    }
}
