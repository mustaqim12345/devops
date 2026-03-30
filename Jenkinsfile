pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name myapp-container myapp'
            }
        }
    }
}
