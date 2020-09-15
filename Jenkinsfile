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
          when {
            not {
              branch 'master'
            }
          }
          steps {
            fileExists 'xpackage.jsonx'
            unstable 'oops'
          }
        }

      }
    }

  }
}
