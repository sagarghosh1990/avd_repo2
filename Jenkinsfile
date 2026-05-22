pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Users\\MONY SAGAR GHOSH\\AppData\\Local\\Programs\\Python\\Python314'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Python') {
            steps {
                bat "${env.PYTHON} --version"
            }
        }

        stage('Extract') {
            steps {
                bat "${env.PYTHON} extract.py"
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
