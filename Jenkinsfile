pipeline {
    agent any
    options {    buildDiscarder(logRotator(numToKeepStr: '03' ) )  }
     
   stages {
      stage ('Compile') {
      steps {  echo 'Hello World'  }
        }
      stage('User Input') {         
          input { message 'User input required', ok: 'Release!',
              parameters {choice(name: 'RELEASE_SCOPE', choices: 'patch\nminor\nmajor', description: 'What is the release scope?')}
                 }
        steps { echo "env: ${env.RELEASE_SCOPE}"  }
                          }
       
    stage ('Code test') {
      steps {
      sh 'cat index2.html'
          
              }
          }
        }
    post {
       always {
           sh  'echo build completed'
         }
     changed {
           sh  'echo build changed'
         }
        
        success {
           sh  'echo build success'
         } 
        unstable {
           sh  'echo build unstable'
         }
       failure {
           sh  'echo build failure'
         }
    }
}
