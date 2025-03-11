pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cpp -o output'
                build 'PES2UG22CS665-1'
            }
        }
        stage('Test') {
            steps {
                sh './output'
                echo 'Test successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        success {
            echo 'Success'
        }
        failure {
            echo 'Failed'
        }
    }
}
