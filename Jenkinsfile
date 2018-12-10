
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
                def msbuild = tool name: 'MSBuild', type: 'hudson.plugins.msbuild.MsBuildInstallation'
                bat "${msbuild} Jenkinstest.sln"
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
