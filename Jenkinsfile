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
                    bat 'docker build -t testingapp-image .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    bat 'docker run -d -p 8095:80 testingapp-image'
                }
            }
        }

    }
}