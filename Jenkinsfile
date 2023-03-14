pipeline {
  agent any
  stages {
    stage('check code') {
      steps {
        git(url: 'https://github.com/jangama3/jenkins1', branch: 'dev')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front-end') {
          steps {
            sh 'cd curriculus-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}