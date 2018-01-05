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
  }
}
