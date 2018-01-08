pipeline {
 agent any
  stages {
    stage('PreStage') {
      steps {           
           echo "prepare..."          
      }
    }  
   stage('experimental') {
        agent{ 
        dockerfile true
      }
    } 
   
    stage('Build Docker Image manually') {    
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
