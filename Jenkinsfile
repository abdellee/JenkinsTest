
pipeline {
    agent any
    stages {
        stage('Checkout code') {
            steps {
                git 'https://github.com/jenkinsci/pipeline-examples.git'
                
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                bat "\"${tool 'MSBuild'}\" Jenkinstest.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"
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
}
