pipeline {
  agent any 
  stages {
    stage('build') {
      steps {
        sh 'pip install -r requirements.txt --user'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}
