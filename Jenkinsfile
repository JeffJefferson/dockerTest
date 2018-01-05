pipeline {
  agent { dockerfile true 
  }
  stages {
    stage('Build') {
      steps {
         docker.build("my-image-name")    
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}
