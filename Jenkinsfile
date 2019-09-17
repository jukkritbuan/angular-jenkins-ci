pipeline {
    agent any
    tools {nodejs "node"}
    stages {
        stage('npm install') {
            steps {
                bat "npm ci"
            }
        }
        stage('e2e tests') {
          steps {
              bat "npm run e2e:ci"
          }
        }
    }
}
