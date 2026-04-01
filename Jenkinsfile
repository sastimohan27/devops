pipeline {
    agent any

    stages {
        stage('Checkout from Local Git') {
            steps {
                git url: 'C:/git/node-docker-app', branch: 'master'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t node-localgit .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run node-localgit'
            }
        }
    }
}
