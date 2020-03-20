//My First Jenkinsfile

node('master'){
  stage('Prepare'){
   checkout scm
   //git 'https://github.com/Martin1196155/hello-world.git' 
  }
  stage('Build'){
    sh 'mvn clean install package'
  }
}





