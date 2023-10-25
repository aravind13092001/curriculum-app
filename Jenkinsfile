pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/aravind13092001/curriculum-app.git', branch: 'dev')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit Test') {
          steps {
            sh 'cd curriculam-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}