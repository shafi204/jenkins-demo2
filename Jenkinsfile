pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'touch build-artifact.txt'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'ls -la'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'pwd'
                sh 'mv build-artifact.txt deployment/'
            }
        }
    }
    
    post {
        always {
            archiveArtifacts artifacts: '**/build-artifact.txt', allowEmptyArchive: true
        }
    }
}

