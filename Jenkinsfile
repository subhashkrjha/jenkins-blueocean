pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello Java'
        bat '''
             date /t
             time /t
            '''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test Step executed.'
          }
        }

        stage('Test parallel') {
          steps {
            echo 'Test Parallel executed.'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed successfully.'
      }
    }

  }
}