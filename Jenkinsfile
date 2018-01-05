pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        app = docker.build("my-nginx")
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
