pipeline {
    agent any
    environment {
        DOCKER_BUILDKIT = "1"
    }
    stages {
        stage("Checkout") {
            steps {
                checkout scm
            }
        }
        stage("Build Docker Image") {
            steps {
                sh "docker build -t hello-node-app ."
            }
        }
        stage("List Image") {
            steps {
                sh "docker images hello-node-app"
            }
        }
    }
}
