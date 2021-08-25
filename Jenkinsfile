pipeline {
  agent any
  
  tools {nodejs "node"}
  
  stages {
    stage('Lint') {
      steps {
        echo 'Linting stage...'
      }
    }
     stage('Build') {
      steps {
        git 'https://github.com/kalwar/null_or_empty.git'
        sh 'npm install'
      }
    }
     stage('Test') {
      steps {
        echo 'Testing our awesome app...'
      }
    }
  }
}
