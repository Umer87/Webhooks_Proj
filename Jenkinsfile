pipeline {
    agent any
    options {    buildDiscarder(logRotator(numToKeepStr: '03' ) )  }
    environment  {        
        Yasir= '33'
        Umer= '45'
                   }
   stages {
      stage ('Compile') {
      steps {  echo 'Hello World'  }
        }
      stage('Example') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "umer,Yasir"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Choose user', description: 'Who should I say hello to?')
                           }
                   }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
                   }
        }     
        stage ('Scripting') {
            steps {  
                script { 
                     if (env.Yasir == '33' && env.Umer == '45')
                             {  sh 'echo Umer and Yasir Ages'}
                    else { echo 'Hello World' }
                     
                    }
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
        unstable {
           sh  'echo build unstable'
         }
       failure {
           sh  'echo build failure'
         }
    }
}
 
