pipeline{
    
 agent any
 stages{
     stage('Build'){
         steps{
             sh "mvn clean package"
         }
     }
  stage('Deploy'){
         steps{
          deploy adapters: [tomcat7(credentialsId: '6656e9f2-5d3d-4515-b904-5defdac3b300', path: '',
          url: 'http://ec2-3-17-203-242.us-east-2.compute.amazonaws.com:8080/')],
          contextPath: 'javawebapp', war: '**/java-web-project.war'
         }
     }     
 }
}
