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
      }
    }
    stage('prod') {
      steps {
        echo 'I am prod'
      }
    }
  }
}