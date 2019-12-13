pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test'
          }
        }

        stage('unity test') {
          steps {
            echo 'unity test'
          }
        }

        stage('integration testing') {
          steps {
            echo 'integration testing'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deplay'
      }
    }

    stage('UAT') {
      parallel {
        stage('UAT') {
          steps {
            echo 'Report'
          }
        }

        stage('Security (DoS resistance)') {
          steps {
            echo 'Security'
          }
        }

        stage('Performance') {
          steps {
            echo 'Performance'
          }
        }

        stage('functionality') {
          steps {
            echo 'functionality'
          }
        }

      }
    }

    stage('Production') {
      steps {
        sleep 5
        echo 'Production'
      }
    }

  }
}