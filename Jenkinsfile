pipeline {
    agent any 
     environment {
            CI = 'true'
        }
    stages {
        stage('Build') {
            steps {
                sh 'npm install @skalwar/null_or_empty --save'
            }
        }
        stage('Test') {
                    steps {
                        sh './scripts/test.sh'
                    }
                }
         stage('Deliver') {
                            steps {
                                sh './scripts/deliver.sh'
                                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                                sh './scripts/kill.sh'
                            }
                        }
          }
       }
