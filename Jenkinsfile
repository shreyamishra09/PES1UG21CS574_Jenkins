pipeline {
  agent any
  
  stages{
    stage('Build') {
      steps {
        script {
          sh 'g++ -o executable main/PES1UG21CS574.cpp'
        }
        echo 'Build stage successful'
      }
    }

    stage('Test') {
      steps {
        script {
          sh './executable'
        }
        echo 'Test Successful'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }

  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
