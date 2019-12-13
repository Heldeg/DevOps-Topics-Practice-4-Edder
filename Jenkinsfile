pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Test') {
      steps {
        echo 'Test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deplay'
      }
    }

    stage('UAT') {
      steps {
        echo 'Report'
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