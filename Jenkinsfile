pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        git(url: 'https://github.com/5P4RK3R/ShowFinder', branch: 'main')
      }
    }

    stage('stage') {
      steps {
        sh 'ls -la'
      }
    }

  }
}