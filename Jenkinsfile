pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building project"
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
