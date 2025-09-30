pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello Jenkins'
    }
    options {
        timeout(time: 1, unit: 'HOURS')
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
                sh """
                    echo "Here i wrote shell-script"
                    echo "$GREETING"
                    sleep 10
                """
            }
        }
    }
    // post build
    post {
        always {
            echo 'i will always say hello pipeline'
        }
        failure {
            echo 'this run when the pipleline is failed, used generally to send some alerts'
        }
        success {
            echo 'i will say hello when pipeline is success'
        }
    }
}