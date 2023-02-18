pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'make -C'
        build job: 'PES1UG20CS184-1'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh ' /var/jenkins_home/workspace/PES1UG20CS184/new_exec'
        echo 'Test Stage Successful'
        }
      }
    }
  stage('Deploy') {
      steps {
        sh 'cat x.txt'
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
