pipeline {
  agent any
  stages {
    stage('Verify') {
      parallel {
        stage('Model Advisor') {
          steps {
            echo 'Running model advisor checks'
          }
        }

        stage('Design Verifier') {
          steps {
            echo 'Checking model for correct architecture'
          }
        }

      }
    }

    stage('Build') {
      steps {
        echo 'Build stage has begun...'
      }
    }

    stage('Test') {
      parallel {
        stage('Test1') {
          steps {
            echo '"Test" stage has begun...'
          }
        }

        stage('Test2') {
          steps {
            echo 'Test1'
          }
        }

        stage('Test3') {
          steps {
            echo 'Test2'
            echo 'Hello'
          }
        }

      }
    }

    stage('Package') {
      parallel {
        stage('Generate Report') {
          steps {
            echo 'Creating report...'
          }
        }

        stage('Store Artifacts') {
          steps {
            echo 'Archiving...'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Complete!'
      }
    }

  }
}