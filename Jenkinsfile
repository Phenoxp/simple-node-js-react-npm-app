pipeline {
    agent any 
    tools {
        nodejs "NodeJS"
    }
    environment {
        CI = 'true'
    }
    stages{
        stage('Build'){
            steps {
                //sh 'npm install'
                bat 'npm install'
            }
        }
        stage('Test') { 
            steps {
                //sh './jenkins/scripts/test.sh' 
                bat 'npm test'
            }
        }
        stage('Deliver'){
            steps {
                //sh 'npm run build'
                bat 'npm run build'
            }
        }
        stage('Deploying'){
            steps {
                //sh 'npm start'
                bat 'npm start'
            }
        }
    }
}