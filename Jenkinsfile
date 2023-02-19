pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ main/newfile.cpp -o new'
        build 'PES2UG20CS333-1'
        echo 'Build Successful'
      }
    }

    stage('Test') {
      steps {
        sh './new'
        echo 'Testing Successful'
      }
    }

    stage('Deploy') {
      when {
        /*expression {
          currentBuild.result == null || currentBuild.result == 'SUCCESS'
        }
      }
      steps {
        echo 'Deployment Successful'
      }*/
    }
  }

  post {
    failure {
      echo 'Pipeline failed'
    }
} }







