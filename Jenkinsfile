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
                sh 'docker run -d -p 5000:5000 myapp'
            }
        }
    }
}
