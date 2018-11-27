pipeline {
    agent {
        docker {
            image 'zenika/alpine-chrome:with-node'
            args '-u 0:0 --entrypoint=""' // set user to root
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "npm install"
            }
        }
        stage('Unit Tests') {
          steps {
              echo 'Unit testing..'
              sh "npm run test:ci"
          }
        }
    }
}
