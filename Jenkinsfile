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
                sh 'docker build -t azure-app-pipeline ./azure-vote"'
            }
        }
    }
}
