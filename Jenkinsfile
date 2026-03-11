pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/RAKSHANSP/AgriConnectFrontend.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('My Sonar Server') {
                    sh 'sonar-scanner'
                }
            }
        }

    }
}
