pipeline {
    agent any
    triggers {
        pollSCM("* * * * *")
            }
   stages {
      stage ('Compile') {
      steps {
        echo 'Hello World'
          exit 1
              }
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
       unsuccessful {
           sh  'echo build unsuccessfil'
         }
    }
}
