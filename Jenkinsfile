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
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    echo 'Building the application...'
                    sh 'npm run build'
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