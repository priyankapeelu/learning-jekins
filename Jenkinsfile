// pipeline {
//   agent any
//
//   options {
//     ansiColor('xterm')
//   }
//
//   environment {
//      ENV_URL = "pipeline.google.com"
//      SSH_CRED = credentials("SSH")
//   }
//
//   triggers {
//     pollSCM('*/2 * * * *')
//   }
//
//   tools {
//     maven 'maven-3.8.5'
//   }
//
//   parameters {
//     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//   }
//
//   stages {
//
//     stage('One') {
//       steps {
//             addShortText background: '', borderColor: '', color: '', link: '', text: 'ONE'
//             sh '''
//               echo hello1
//               echo hello2
//               echo ENV_URL = ${ENV_URL}
//             '''
//       }
//     }
//     stage('Two') {
//       options {
//         ansiColor('xterm')
//         }
//       environment {
//          ENV_URL = "stage.google.com"
//       }
//
//        input {
//          message "Should we continue?"
//          ok "Yes, we should."
//          submitter "alice,bob"
//          parameters {
//            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//          }
//        }
//
//       steps {
//         echo "Two"
//         sh 'echo ENV_URL = ${ENV_URL}'
//         sh 'env'
//         echo '\033[34mHello\033[0m \033[33molorful\033[0m \033[35mworld!\033]0m'
//         sh 'echo -e "\\e[31mHello"'
//         //sh 'terraform apply -auto-approve'
//         sh 'mvn --version'
//       }
//     }
//   }
//
// }

pipeline {
  agent any

  stages {

    stage('Parallel') {
      parallel {

        stage('One') {
          steps {
            sh 'sleep 10'
          }
        }

         stage('Two') {
           steps {
             sh 'sleep 10'
              }
            }

            stage('Three') {
              steps {
                sh 'sleep 10'
              }
            }

         }
       }

    }
  }
