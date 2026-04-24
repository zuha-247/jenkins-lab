pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    parameters {
        booleanParam(
            name: 'executeTests',
            defaultValue: true,
            description: 'Run Test Stage?'
        )
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
            when {
                expression { params.executeTests == true }
            }
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
