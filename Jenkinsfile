pipeline {
    agent any
    triggers {
        pollSCM("* * * * *")
            }
   stages {
      stage ('Compile') {
      steps {
        echo 'Hello World'
         
              }
        }
      
    stage ('Code test') {
      steps {
      sh 'cat index2.html'
          exit 1
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
