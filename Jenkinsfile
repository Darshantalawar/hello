pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Darshantalawar/hello.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building on macOS'
                sh 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running tests'
                // Add test commands here
            }
        }

        stage('Run Application') {
            steps {
                sh 'echo Running Hello.java'
                sh 'java Hello'
            }
        }
    }
}

