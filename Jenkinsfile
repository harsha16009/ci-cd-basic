pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                deleteDir()
            }
        }

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                sh 'cat index.html > output.html'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'output.html'
        }
    }
}
