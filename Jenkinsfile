pipeline {
    agent any

 
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh '''
                        docker build -t python-app .
                    '''
                }
            }
        }
 
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d --name python-app-cont python-app'
                }
            }
        }
    }