pipeline {
    agent any

    environment {
        PYTHON = '"C:\\Users\\MONY SAGAR GHOSH\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" --version'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Python') {
            steps {
                bat "${env.PYTHON}"
            }
        }

        stage('Extract') {
            steps {
                bat "${env.PYTHON} extract_data.py"
            }
        }
    }

    