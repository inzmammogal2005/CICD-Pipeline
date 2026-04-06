pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/inzmammogal2005/CICD-Pipeline.git'
            }
        }

        stage('Build Docker') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run App') {
            steps {
                sh '''
                docker stop myapp || true
                docker rm myapp || true
                docker run -d -p 5000:5000 --name myapp myapp
                '''
            }
        }
    }
}
