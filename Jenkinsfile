pipeline {
    agent any
    stages {
        stage('vcs') {
            steps {
                git branch: 'dev', url:'https://github.com/AnasAnsar1/saleor.git'
            }
        }
        stage('Image_build') {
            steps {
                sh 'docker image build -t anasansarii/saleor:jnkdev .'
            }
        }
        stage('Image_push') {
            steps {
                sh 'docker image push anasansarii/saleor:jnkdev'
            }
        }
    }
}