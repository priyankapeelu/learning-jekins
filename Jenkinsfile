pipeline {
  agent any

  stages {

    stage('One') {
      steps {
        addBadge icon: '', id: '', link: '', text: 'ONE'
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