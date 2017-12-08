pipeline {
  agent {
    node {
      label 'jslave'
    }
    
  }
  stages {
    stage('Fetch code') {
      steps {
        parallel(
          "Fetch code": {
            sh 'echo "ini step fetch code"'
            git(url: 'http://172.17.0.30/aasmarani/testing-project.git', branch: 'master', credentialsId: 'gitlab_docker')
            
          },
          "hello ": {
            sh 'echo "hello bajau"'
            echo 'hahaha'
            
          }
        )
      }
    }
    stage('Check File') {
      steps {
        sh 'ls -la'
      }
    }
  }
}