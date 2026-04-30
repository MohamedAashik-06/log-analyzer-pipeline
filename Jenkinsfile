pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/YOUR-USERNAME/log-analyzer-pipeline.git'
            }
        }

        stage('Run Python Script') {
            steps {
                bat 'python analyzer.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
