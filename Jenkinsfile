pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/ibrahimcsharp/Testingapp'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t testingapp-image .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d -p 8090:80 testingapp-image'
                }
            }
        }

    }
}