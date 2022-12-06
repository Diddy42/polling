pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                pwd
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