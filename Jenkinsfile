pipeline {
  agent any
  stages {
    stage('check code') {
      steps {
        git(url: 'https://github.com/jangama3/jenkins1', branch: 'dev')
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}