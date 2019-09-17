pipeline {
    agent {
        docker {
            image 'avatsaev/angular-chrome-headless'
        }
    }
    stages {
        stage('npm install') {
            steps {
                sh "npm install"
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
