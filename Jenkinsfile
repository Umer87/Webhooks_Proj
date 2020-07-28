pipeline {
    agent any
    trigger {
        cron("* * * * *")
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
