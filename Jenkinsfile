// My First Jenkinsfile

node('master'){
  // def mvnHome=tool'M2_HOME'
  stage('Prepare'){
   checkout scm
   //git 'https://github.com/Martin1196155/hello-world.git' 
  }
  stage('Build'){
    withMaven(
     maven : "M2_HOME"
    ){
    sh 'mvn clean install package'
    }
  }
  try{
  stage('Test'){
  withMaven(
    maven : "M2_HOME"
    ){
    sh 'mvn test'    
  }
  }  
 }
  finally{
        junit '**/target/surefire-reports/*.xml'
        jacoco()
    }
  
  stage('Sonar'){
  withMaven(
    maven : "M2_HOME"
    ){
    sh 'mvn clean install sonar:sonar'   
  }
  }
  
  stage('Tomcat_Deployment'){
  sshagent(['Connect-Tomcat']) {
    sh 'scp -o StrictHostKeyChecking=no **/target/*.war ec2-user@172.31.40.62:/opt/tomcat/webapps'  
  }
}
}
 




