pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/ArunkumarElak/MERN-Stack.git'
            }
        }
        stage('Deploy Application') {
            steps {
                sh 'docker compose down --remove-orphans'
                sh 'docker compose up -d --build'
            }
        }
    }
}