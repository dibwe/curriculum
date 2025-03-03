pipeline {
  agent any
  stages {
    stage('Checkout Code ') {
      steps {
        git(url: 'https://github.com/dibwe/curriculum', branch: 'main')
      }
    }

    stage('List code') {
      parallel {
        stage('List code') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Font-end unit Test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}