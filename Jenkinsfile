pipeline {
  agent any
stages {

  stage('git-checkout') {
  steps {
git 'https://github.com/vijay2181/maven-wa...
           }
}
  
  stage('environment-setting') {
             steps {
                  script {
                       env.BUILD = "yes" // Setting env variable for Build 
                             }
                       }
                 }


   stage('Build')  {

   when {environment name: 'BUILD', value: 'yes'}
   steps { 
               echo "Building artifacts ..."
               sh "mvn clean package "
               }

             }
}
}
