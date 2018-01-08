pipeline {
 agent any
  stages {
    stage('Build Docker Image') {
       agent{ 
        dockerfile true
      }
      steps {
           bat "docker build -t test ."
      }
    }  
    stage('Test Docker Image') {
      steps {           
           bat "hh http://localhost:82"          
      }
    }  
    
    stage('Publish Docker Image') {
      steps {
           bat "docker tag test localhost:5000/hello-nginx"
           bat "docker push localhost:5000/hello-nginx"
      }
    }  
    
   
  }
}
