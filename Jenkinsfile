pipeline {
    agent {
        label "Jenkins"
    }
    triggers {
        pollSCM '*/2 * * * *'
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
                python3 delivery.py
                '''
            }
        }
    }
}