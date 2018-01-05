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
           bat "docker run -p 82:80 test"
      }
    }  
  }
}
