pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Repository already checked out by Jenkins.'

            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-jenkins-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name flask_app flask-jenkins-demo'
            }
        }
    }
}

