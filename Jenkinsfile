pipeline {
    agent any
    stages {
        stage('Bonjour') {
            steps {
                echo 'Bonjour depuis Jenkins !'
            }
        }
        stage('Date') {
            steps {
                sh 'date'
            }
        }
        stage('Whoami') {
            steps {
                sh 'whoami'
            }
        }
    }
}
