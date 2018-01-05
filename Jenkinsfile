pipeline {
  agent any
  stages {
    stage('DockerTest') {
      steps {
           bat "docker build -t test ."
      }
    }  
  }
}
