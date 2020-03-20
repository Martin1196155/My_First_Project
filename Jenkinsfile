//My First Jenkinsfile

node('master'){
 def mvnHome
  stage('Prepare'){
   checkout scm
   //git 'https://github.com/Martin1196155/hello-world.git' 
  }
  stage('Build'){
    mvnHome=tools'M2_HOME'  
    sh 'mvn clean install package'
  }
}





