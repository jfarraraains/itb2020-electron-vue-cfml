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
            unstable 'awe, package.json missing'
          }
        }

      }
    }

  }
}