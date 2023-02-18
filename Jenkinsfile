pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Run build commands
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                // Run tests
                sh 'npm run test'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy application
                sh 'npm run deploy'
            }
        }
    }
    
    post {
        always {
            // Display message if pipeline failed
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
