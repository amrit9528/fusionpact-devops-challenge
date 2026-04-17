pipeline {
    agent { label 'docker' }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/amrit9528/fusionpact-devops-challenge.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                docker compose up -d --build
                '''
            }
        }

    }
}
