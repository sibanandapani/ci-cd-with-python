pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
        sh 'pip3 install -r requirements.txt --user'
      }
    }
    stage('Test') {
      steps {
        sh 'python3 test.py'
      }   
    }
    stage('Deploy') {
      steps {
        sh 'python3 app.py &'
        sh 'sleep 500'
      }   
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
