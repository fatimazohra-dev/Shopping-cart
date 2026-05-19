pipeline {
    agent any

    stages {

        stage('Build Maven') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t fatimaazohra/shopping-cart:latest .'
            }
        }

        stage('Docker Push') {
            steps {
                script {
                    docker.withRegistry('', 'dockerhub') {
                        sh 'docker push fatimaazohra/shopping-cart:latest'
                    }
                }
            }
        }
    }
}
