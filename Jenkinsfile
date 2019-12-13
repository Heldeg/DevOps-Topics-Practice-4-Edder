pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        libraryResource 'dependence'
      }
    }

    stage('Test') {
      steps {
        junit 'test'
        catchError() {
          build 'Sol Error'
        }

      }
    }

    stage('Deploy') {
      steps {
        node(label: 'Funcion')
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
        input 'All is ok'
      }
    }

  }
}