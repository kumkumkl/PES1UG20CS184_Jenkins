pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'make -C new'
        echo 'Build Stage Successful'
        build job: 'PES1UG20CS184-1'
      }
    }
  }
    stage('Test') {
      steps {
        sh ' /var/jenkins_home/workspace/PES1UG20CS184/new/new_exec'
        echo 'Test Stage Successful'
        }
      }
    }
  stage('Deploy') {
      steps {
        echo 'Deployment Successful'
        sh 'cat x.txt'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
