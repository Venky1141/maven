pipeline {
 agent {label ubuntu}
    tools {
        maven 'maven'
        jdk 'java'
    } 
stages {
    stage('git clone') {
       steps {
         echo 'git clone'
         git 'https://github.com/rangareddy7/devops111.git'
        }
      }  
      stage('build') {
         step{
             echo "maven build"
             sh 'mvn clean'
             sh 'mvn compile'
             sh 'mvn test'
             sh 'mvn package'
             sh 'mvn install'
           }
        }   
   }
}
