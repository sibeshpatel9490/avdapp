pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git url:'https://github.com/sibeshpatel9490/avdapp.git', branch:'main'
            }
        }
        stage('Build Image') {
            steps {
                bat 'docker build -t myimage'
            }
        }
        stage('Create Container') {
            steps {
                bat 'docker run -d -p 8501:8501 myimage'
            }
        }
    }
}