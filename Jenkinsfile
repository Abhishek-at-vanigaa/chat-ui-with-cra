pipeline {
  agent none
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

    stage('login to docker hub') {
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUBB_PASSWORD'
      }
    }

  }
  environment {
    DOCKERHUB_USER = 'abishek.k@vanigaa.in'
    DOCKERHUB_PASSWORD = 'w6dmSFNYLWBqh!HE'
  }
}