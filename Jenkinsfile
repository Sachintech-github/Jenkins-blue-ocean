pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''ls
date
pwd'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'this is test step'
          }
        }

        stage('test parallelly') {
          steps {
            echo 'print message same'
          }
        }

        stage('QA TEST') {
          steps {
            echo 'test code'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed'
      }
    }

  }
}