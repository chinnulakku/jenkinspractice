pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    // environment {
    //     GREETING = 'Hello Jenkins'
    // }
    // options {
    //     timeout(time:1 unit: 'HOURS')
    //build
    stages {
        stage('Build') {
            steps {
                echo 'building stage ..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing stage ..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying stage..'
            }
        }
    }
    // post build
    post {
        always {
            echo 'i will always say hello pipeline'
        }
    }
}