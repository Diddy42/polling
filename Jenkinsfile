pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'pipenv install'
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