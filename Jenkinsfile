pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git https://github.com/saiusha30/flask-jenkins-test-demo.git
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

