pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        git(url: 'https://github.com/5P4RK3R/ShowFinder', branch: 'main')
      }
    }

    stage('stage') {
      parallel {
        stage('stage') {
          steps {
            sh 'ls -la'
          }
        }

        stage('unit test') {
          steps {
            sh 'npm i && npm run test'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f Dockerfile .'
      }
    }

  }
}