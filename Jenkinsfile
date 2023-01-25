pipeline {
  agent any
stages {

  stage('git-checkout') {
  steps {
git 'https://github.com/donpasscall/maven-war-project1.git'
}
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
