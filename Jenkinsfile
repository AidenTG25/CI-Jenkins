pipeline {
    agent any
    tools {
            nodejs 'NodeJS-20' // Use the name you defined in Tools
        }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/AidenTG25/CI-Jenkins.git'
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