pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Hello World') {
            steps {
                sh 'python3 helloworld.py'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 Test.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded: all tests passed.'
        }
        failure {
            echo 'Pipeline failed: check the Console Output.'
        }
    }
}
