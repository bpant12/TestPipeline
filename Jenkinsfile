pipeline {
  agent any
  stages {
    stage('qe') {
      parallel {
        stage('qe') {
          steps {
            echo 'I am QE'
          }
        }
        stage('qe1') {
          steps {
            echo 'QE1 message'
          }
        }
      }
    }
    stage('Stage') {
      steps {
        echo 'I am stage'
        retry(count: 3) {
          input(message: 'Do you want to proceed?', id: '1', ok: 'yes', submitter: 'bp', submitterParameter: 'b')
        }

      }
    }
    stage('prod') {
      steps {
        echo 'I am prod'
      }
    }
  }
}