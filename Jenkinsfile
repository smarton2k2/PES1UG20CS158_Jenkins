pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
      
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
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
