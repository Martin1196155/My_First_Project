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
}





