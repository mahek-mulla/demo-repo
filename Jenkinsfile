pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mahek-mulla/demo-repo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Building...'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Running tests...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
