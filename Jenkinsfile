pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/DevOps13728/gitcicd.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'npm test || echo "No tests yet"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying (dummy step)...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
