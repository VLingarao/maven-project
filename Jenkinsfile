pipeline {
    agent any

    tools {
        maven 'maven-3.9'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging artifact'
                sh 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application (dummy)'
                sh 'echo Deployment completed'
            }
        }
    }

    post {
        success {
            echo 'Build SUCCESS'
        }
        failure {
            echo 'Build FAILED'
        }
    }
}
