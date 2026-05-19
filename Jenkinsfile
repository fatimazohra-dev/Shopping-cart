stage('Docker Push') {
    steps {
        script {
            docker.withRegistry('', 'dockerhub') {
                sh 'docker push fatimaazohra/shopping-cart:latest'
            }
        }
    }
}
