pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }

    stage('Test stuff') {
      parallel {
        stage('Test Firefox') {
          steps {
            sh 'echo \'Testing Firefox\''
          }
        }

        stage('Test Chrome') {
          steps {
            sh 'echo \'Testing Chrome\'; exit 1'
          }
        }

        stage('Test Other') {
          steps {
            sh 'echo "Testin Other"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}
