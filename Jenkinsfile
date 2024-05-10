pipeline {
    agent any
    triggers {
        pollSCM '*/5 * * * *'
    }
    stages {
        stage("Build") {
            steps {
                echo "Building.."
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 helloworld.py
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}