pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Build') {

            when {
                expression {
                    BRANCH_NAME == 'prod'
                }
            }
            steps {
                echo 'Building..'
            }
        }

        stage('Deploy') {
             when {
                expression {
                    BRANCH_NAME == 'prod'
                }
            }
            steps {
                echo 'Deploying....'
            }
        }
    }
}