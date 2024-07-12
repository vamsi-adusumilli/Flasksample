pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub
                git 'https://github.com/vamsi-adusumilli/Flasksample.git'
            }
        }
        
        stage('Setup Environment') {
            steps {
                // Navigate to 'my-website' directory
                dir('my-website') {
                    // Install dependencies if needed (adjust as per your project)
                    sh 'pip install -r requirements.txt'
                }
            }
        }
        
        stage('Run Flask App') {
            steps {
                // Start Flask application
                dir('my-website') {
                    sh 'python app.py &'
                }
            }
        }
    }
}
