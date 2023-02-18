pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Run build commands here
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                // Run test commands here
                sh 'npm run test'
            }
        }
        stage('Deploy') {
            steps {
                // Run deployment commands here
                sh 'npm run deploy'
            }
        }
    }
    
    post {
        always {
            // Display "pipeline failed" if any of the stages failed
            script {
                if (currentBuild.currentResult == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
