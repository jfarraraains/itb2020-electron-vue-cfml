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
              fileExists 'xpackage.jsonx'
            }
          }
          steps {
            unstable 'oops, package.json missing'
          }
        }

      }
    }

  }
}
