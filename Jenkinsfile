pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                build 'PES1UG22CS403-1'
                sh 'g++ task5.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}