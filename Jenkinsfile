pipeline {
  agent any
  stages {
    stage('Checkout Code ') {
      steps {
        git(url: 'https://github.com/dibwe/curriculum', branch: 'main')
      }
    }

    stage('List code') {
      steps {
        sh 'ls -la'
      }
    }

  }
}