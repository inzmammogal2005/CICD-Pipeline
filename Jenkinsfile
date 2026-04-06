stage('Run App') {
    steps {
        sh 'docker rm -f myapp-container || true'
        sh 'docker run -d -p 5000:5000 --name myapp-container myapp'
    }
}
