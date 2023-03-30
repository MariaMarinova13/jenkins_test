pipeline {
    agent {
        node {
            label 'docker-agent-python'
            }
      }

    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd test_app
                pip install fire
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                cd myapp
                python3 hello.py
                python3 hello.py --name=Mimi
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