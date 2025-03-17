pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ PES1UG22CS623.cpp -o PES1UG22CS623'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS623'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
