pipeline {
    agent any
    stages {
      steps {
        echo 'Building pipeline'
        sh 'touch build-artifact.txt'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing part of the pipeline'
        sh 'ls -la'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying part of the pipeline'
        sh 'pwd'
        sh 'mv build-artifact.txt deploymeny/'
      }
    }

post {
  always {
    archiveArtifacts artifacts: '**/build-artifact.txt', allowEmptyArchive: true
  }
}
}

