//My First Jenkinsfile

node('master'){
 def mvnHome
  stage('Prepare'){
   checkout scm
   //git 'https://github.com/Martin1196155/hello-world.git' 
  }
  stage('Build'){
    mvnHome=tool'M2_HOME'  
    sh 'mvn clean install package'
  }
}




