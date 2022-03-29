pipeline {
  agent any


  environment {
     ENV_URL = "pipeline.google.com"
     SSH_CRED = credentials("SSH")
  }

  stages {

    stage('One') {
      steps {
            addShortText background: '', borderColor: '', color: '', link: '', text: 'ONE'
            sh '''
              echo hello1
              echo hello2
              echo ENV_URL = ${ENV_URL}
            '''
      }
    }
    stage('Two') {
      environment {
         ENV_URL = "stage.google.com"
      }
      steps {
        echo "Two"
        sh 'echo ENV_URL = ${ENV_URL}'
        sh 'env'
        echo '\033[34mHello\033[0m \033[33molorful\033[0m \033[35mworld!\033]0m'
      }
    }

  }

}