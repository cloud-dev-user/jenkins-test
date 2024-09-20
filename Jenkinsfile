pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo" this build is successful" '
      }
    }

    stage('Test') {
      steps {
        sh 'echo" this test is successful'
      }
    }

    stage('Notify') {
      parallel {
        stage('Notify') {
          steps {
            sh 'Echo" notify developer" '
          }
        }

        stage('deploy') {
          steps {
            sh 'echo " deploy to the DEV environment" '
          }
        }

      }
    }

    stage('deploy to prod') {
      steps {
        sh 'echo " deploy to prod" '
      }
    }

  }
}