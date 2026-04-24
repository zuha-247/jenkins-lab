pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        VERSION = "1.0"
    }

    stages {
        stage('Build') {
            steps {
                echo "Building version ${VERSION}"
                bat 'mvn --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Finished'
        }
    }
}
