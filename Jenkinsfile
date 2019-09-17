pipeline {
    agent {
        docker {
            image 'avatsaev/angular-chrome-headless'
        }
    }
    tools {nodejs "node"}
    tools {docker "docker"}
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
