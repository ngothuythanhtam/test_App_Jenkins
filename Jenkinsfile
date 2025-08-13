pipeline{
    agent any

    tools {
        nodejs 'NodeJS_24.5.0'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    echo 'Checking out the code...'
                    checkout scm
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'node -v'
                    sh 'npm -v'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'npm run build'
                    echo 'Building the application...'
                }
            }
        }
        // stage('Deploy') {
        //     steps {
        //         script {
        //             echo 'Deploying the application...'
        //             sh 'npm start'
        //         }
        //     }
        // }
    }
}