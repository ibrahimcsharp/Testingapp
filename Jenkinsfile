pipeline {
    agent any
   
    stages {
        stage('Clone Repository')
        steps{
           git 'https://github.com/ibrahimcsharp/Testingapp' 
        }
    }

    stages {
        stage('Build Docker Image')
        steps{
           script {
            sh 'docker build -t testingapp-image .'
           } 
        }
    }

    stages {
        stage('Run Docker Image')
        steps{
           script {
            sh 'docker run -p 8090:80 testingapp-image'
           } 
        }
    }
}