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
    stage ('push artifact') {
            steps {
                sh 'mkdir archive'
                run git archive main --format=zip --output=python.zip > archive/test.txt
                zip zipFile: 'test.zip', archive: false, dir: 'archive'
                archiveArtifacts artifacts: 'test.zip', fingerprint: true
            }
        }
  }
  }

