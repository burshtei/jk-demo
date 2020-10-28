pipeline {
    agent any

    stages {
        stage('Stage 01') {
            steps { 
                git url: 'https://github.com/burshtei/jk-demo.git'
            }
        }
        stage('Stage 02'){
            steps { 
                sh 'npm install'
            }
        }
        stage('Stage 03'){
            steps {
                sh 'npm test'
            }
        }
        stage('Stage 04'){
            steps { 
                sh 'npm run build'
            }
        }
        stage('Stage 05'){
            steps {
                archiveArtifacts artifacts: '*.zip'
            }
        }
    }
}
