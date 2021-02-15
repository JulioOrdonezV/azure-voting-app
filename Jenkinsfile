pipeline {
    agent any

    stages {
        stage('verify branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('docker build') {
            steps {
                sh 'docker build -t julioordonezv/azure-app-pipeline ./azure-vote'
            }
        }
        stage('docker push') {
            steps { 
                script {
                    docker.withRegistry('https://index.docker.io/v1/', 'DockerHub-secret') {

                    def customImage = docker.image("julioordonezv/azure-app-pipeline")
                    customImage.push()
                   }
                }
            }
        }
    }
}
