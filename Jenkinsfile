pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'whoami'
            }
        }
        stage('Test') { 
            steps {
                echo 'testing'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deploying'
            }
        }
    }
}