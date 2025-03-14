pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS384-1'
                sh 'g++ main.cp -o output'
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
