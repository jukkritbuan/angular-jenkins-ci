pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
    }
    }
     environment {
        CI = 'true' 
    }
    stages {
        stage('npm install') {
            steps {
                sh "npm ci"
            }
        }
        stage('Unit Tests') {
          steps {
              sh "npm run test:ci"
          }
        }
        stage('e2e tests') {
          steps {
              sh "npm run e2e:ci"
          }
        }
    }
}
