pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'make -C main'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh ' /var/jenkins_home/workspace/PES1UG20CS184/main/hello_exec'
        echo 'Test Stage Successful'
        }
      }
    }
  stage('Deploy') {
      steps {
        sh 'make -C main'
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
