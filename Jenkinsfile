pipeline {
  agent any
  stages {
    stage('Build Docker Image') {
      steps {
           bat "docker build -t test ."
      }
    }  
    stage('Run Docker Image') {
      steps {
           bat "docker run -d -p 82:80 test"
      }
    }  
    
    stage('Publish Docker Image') {
      steps {
           bat "docker tag test localhost:5000/hello-nginx"
      }
    }  
    
   
  }
}
