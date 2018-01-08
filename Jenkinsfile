pipeline {
 agent any
  stages {
    stage('PreStage') {
      steps {           
           echo "prepare..."          
      }
    }  
   /* 
   stage('experimental') {
        agent{ 
        dockerfile true
      }
     steps {           
           echo "try building dockerfile using agent..."           
      }
    } 
    */
   
    stage('Build Docker Image manually') {    
      steps {
      
           bat "docker build -t test -f "Dockerfile" ."
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
