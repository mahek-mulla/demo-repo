pipeline {
    agent any
    environment {
       MY_SECRET = credentials('test-secret')
   }

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
        stage('Test secret') {
           steps {
               sh 'echo "The secret is: $MY_SECRET ......technically should not be visible"'
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
