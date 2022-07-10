pipeline {
  agent any 
  stages {
    stage('build') {
      steps {
        sh 'pip3 install -r requirements.txt --user'
      }
    }
    stage('test') {
      steps {
        sh 'python3 test.py'
      }   
    }
  }
}
