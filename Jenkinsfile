pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Deployment building'
      }
    }
    stage('Test') {
      steps {
        echo 'Deployment testing'
      }
      
    }
    stage('Deploy') {
      steps {
        echo 'Deployed'
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
