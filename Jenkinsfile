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
   stage('Sonar CodeAnalysis') {
     withMaven(jdk: 'java', maven: 'maven') {
        sh 'mvn sonar:sonar -Dsonar.projectKey=maven_app -Dsonar.organization=sonarcloud-project -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=af00f8a29fa7ccd78ec657bdc0bca796d0c8d330'
      }  
    }
   stage('Package to Jfrog') {
    withMaven(jdk: 'java', maven: 'maven') {
     sh 'mvn package'
      }
    }
   
   stage('Deploy to Dev') {
     
    }
   stage('Automation Testing') {
     
    }
   stage('Deploy to Test') {
     
    }
   stage('Smoke Testing') {
     
    }
   stage('Deploy to Prod') {
     
    }
   stage('Acceptance Testing') {
     
    }
}
