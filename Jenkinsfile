pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('nodejs-demoapp')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    docker.image('nodejs-demoapp').run('-d -p 3000:3000')
                }
            }
        }
    }
}

