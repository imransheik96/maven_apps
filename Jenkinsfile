node {
    stage('Code Checkout') { // for display purposes
     echo 'Checout Code and clone it inside jenkins workspace.'
     git 'https://github.com/imransheik96/maven_apps.git'
   }
   stage('Build Test & Package') {
      echo 'Build the package'
      withMaven(jdk: 'java', maven: 'maven') {
       sh 'mvn clean compile'
     }
   }
   stage('Artifacts') {
       echo 'package the project artifacts..'
       withMaven(jdk: 'java', maven: 'maven') {
       sh 'mvn package'
     }
   
   }
   stage('Deploy to Dev'){
       echo 'Deploy to Dev environment'
   }
   stage('Deploy to Test'){
       echo 'Deploy to Test environment'
   }
      stage('Test Automation'){
       echo 'Deploy to Dev environment'
   }
   
}
