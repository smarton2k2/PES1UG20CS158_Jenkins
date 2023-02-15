pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build'
      }
    }
    stage('Test') {
      steps {
        sh 'docker test'
      }
      
    }
    stage('Deploy') {
      steps {
        sh 'docker deploy'
      }
    }
  }
  post {
    always {
      echo 'Deployment pending'
    }
    success {
      echo 'Pipeline succeeded!'
    }
    failure {
      echo 'Pipline failed!'
    }
  }
}
