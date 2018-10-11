node{
  stage('download'){
   git credentialsId: '29aecd70-08a6-490d-b8be-e21f3f5cef39', url: 'http://35.201.147.92/student-development/student.git'
   }
   
  stage('compile'){
   sh 'mvn compile'
   }
   
  stage('code-analysis'){
  sh 'mvn sonar:sonar -Dsonar.host.url=http://35.234.46.8:9000 -Dsonar.login=0896ba6e24cf555e4fb1be426c3b4f2b9a57c6a7'
  }
  
  stage('package'){
  sh 'mvn package'
  }
  
  stage('deploy-nexus'){
  sh 'mvn deploy'
  }
  
  
}


