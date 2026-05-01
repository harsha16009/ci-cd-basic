pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'echo Hello from Jenkins > output.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing project...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying project...'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'output.txt', fingerprint: true
        }
    }
}
