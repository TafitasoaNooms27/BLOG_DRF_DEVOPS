pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Build') {
            steps {
                echo 'Building..'
            }
        }

        stage('Deploy') {
            when {
                anyOf {
                    branch 'master'
                    branch 'dev'
                    branch 'preprod'
                    branch 'prod'
                }
            }
            steps {
                echo 'Deploying....'
            }
        }
    }
}