pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            echo 'Hello Blue Ocean'
          }
        }

        stage('more') {
          steps {
            fileExists 'xpackage.jsonx'
            unstable 'oops'
          }
        }

      }
    }

  }
}