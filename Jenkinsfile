node {
   
   stage('Code Checkout') { 
     git credentialsId: 'github', url: 'https://github.com/imransheik96/maven_apps.git' 
    }
   stage('Build') {
    withMaven(jdk: 'java', maven: 'maven') {
     sh 'mvn clean compile'
      }
    }
   stage('Unit Test run') {
    withMaven(jdk: 'java', maven: 'maven') {
     sh 'mvn test'
      } 
    }
   stage('Packageto Jfrog') {
    withMaven(jdk: 'java', maven: 'maven') {
     sh 'mvn package'
      }
    }
   stage('Deploy to Dev') {
     
    }
   stage('Deploy to Test') {
     
    }
   stage('Deploy to Prod') {
     
    }
}
