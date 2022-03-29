pipeline {
  agent any

  stages {

    stage('One') {
      steps {
        sh '''
          echo hello1
          echo hello2
        '''
      }
    }

    stage('Two') {
      steps {
        echo "Two"
      }
    }
  }

}