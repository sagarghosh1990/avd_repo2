node {
    def PYTHON = '"C:\\Users\\MONY SAGAR GHOSH\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" --version'

    try {
        stage('Checkout') {
            checkout scm
        }

        stage('show python version') {
            bat "${PYTHON}"
        }

        stage('run python program') {
                bat "${PYTHON} extract_data.py" 
        } 

    }
     catch (err) {
        echo "Pipeline failed: ${err}"
    }
}
