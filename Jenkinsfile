pipeline {
  agent any
  stages {
    stage('Verify') {
      steps {
        echo 'Verify stage has begun...'
      }
    }

    stage('Build') {
      steps {
        echo 'Build stage has begun...'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo '"Test" stage has begun...'
          }
        }

        stage('Test1') {
          steps {
            echo 'Test1'
          }
        }

        stage('Test2') {
          steps {
            echo 'Test2'
            echo 'Hello'
          }
        }

      }
    }

    stage('Package') {
      parallel {
        stage('Package') {
          steps {
            echo 'Creating report...'
          }
        }

        stage('Archive') {
          steps {
            echo 'Archiving...'
          }
        }

      }
    }

    stage('Finish') {
      steps {
        echo 'Complete!'
      }
    }

  }
}