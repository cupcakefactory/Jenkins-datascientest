pipeline {
    agent any
    environment {
        APP_NAME = 'cupcake-factory'
        VERSION = '1.0'
    }
    stages {
        stage('Bonjour') {
            steps {
                echo "Démarrage du pipeline pour ${APP_NAME} version ${VERSION}"
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
        stage('Deploy') {
            when {
                expression { 
                    env.GIT_BRANCH == 'origin/master' 
                }
            }
            steps {
                echo "Déploiement de ${APP_NAME} sur master !"
            }
        }
    }
    post {
        success {
            echo "✅ Pipeline terminé avec succès !"
        }
        failure {
            echo "❌ Pipeline en échec !"
        }
    }
}
