pipeline {
    // Telling Jenkins to run the pipeline on any available agent.
    agent any

    // This is the pipeline. It is a series of stages that Jenkins will run.
    stages {
        // This state is telling Jenkins to checkout the source code from the source control management system.
        stage('Checkout') {
            steps {
                git 'https://github.com/kumar155/form-validations.git'
                checkout scm
            }
        }
        
        // This stage is telling Jenkins to run the tests in the client directory.
        stage('Install') {
            steps {
                 sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                 sh 'npm run build'
            }
        }
    }
}
