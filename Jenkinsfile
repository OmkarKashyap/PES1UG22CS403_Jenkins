pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

                sh 'g++ task5.cpp -o PES1UG22CS403-1'
                sh 'make hello_exec'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22CS403-1'
                sh './hello_exec'
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
            echo 'Pipeline failed!'
        }
    }
}
