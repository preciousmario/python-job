pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'python3 check_endpoint.py'
      }
    }
    stage('build') {
      steps {
        echo "test"
      }
    }  
    stage ('clean') {
            steps {
                sh 'mkdir result'
                sh 'cd result'
                sh 'git archive main --format=zip --output=report.zip'
                
            }
        }
  }
  }

