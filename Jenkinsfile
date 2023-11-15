pipeline {
  agent any
  stages {
    stage('code chekcout') {
      steps {
        git(url: 'https://github.com/Abhishek-at-vanigaa/chat-ui-with-cra', branch: 'main')
      }
    }

    stage('list dir') {
      parallel {
        stage('list dir') {
          steps {
            sh 'ls -la'
          }
        }

        stage('npm package install') {
          steps {
            sh 'npm install '
          }
        }

      }
    }

  }
}