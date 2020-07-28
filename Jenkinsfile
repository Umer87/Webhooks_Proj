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
              }
          }
  }
}
