pipeline {
    agent {
        docker {
            image 'avatsaev/angular-chrome-headless'
            args '-u 0:0 --entrypoint=""' // set user to root
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "rm -rf node_modules && npm install"
            }
        }
        stage('Unit Tests') {
          steps {
              echo 'Unit testing..'
              sh "npm run test:ci"
          }
        }
        stage('e2e tests') {
          steps {
              echo 'Unit testing..'
              sh "npm run e2e:ci"
          }
        }
    }
}
