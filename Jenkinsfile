pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git clone "https://github.com/AidenTG25/CI-Jenkins.git"
            }
        }
        stage('Install Dependencies') {
            steps {
                bat "npm install"
            }
        }
        stage('Run App') {
            steps {
                bat 'node app.js'
            }
        }
        stage('Test App') {
            steps {
                bat 'node test.js'
            }
        }
    }
    post{
        success{
            echo "CI Pipeline Success"
        }
        failure{
            echo "CI Pipeline Failure"
        }
    }
}