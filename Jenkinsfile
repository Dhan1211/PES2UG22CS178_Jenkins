pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Dhan1211/PES2UG22CS178_Jenkins.git'
            }
        }
        stage('Build ') {
            steps {
                sh 'g++ hello.cpp -o output'
                echo 'Build completed successfully'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
    }
    post {
        failure {
            echo 'Fail !!!!!'
        }
    }
}
