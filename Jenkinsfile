pipeline {
    agent {
        docker {
            image 'zenika/alpine-chrome'
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
        stage('Test') {
            steps {
                echo 'Deploying..'
            }
        }
    }
}
