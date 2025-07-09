pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/MarcoMaged024/devops-nodejs-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-nodejs-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 devops-nodejs-app'
            }
        }
    }
}
