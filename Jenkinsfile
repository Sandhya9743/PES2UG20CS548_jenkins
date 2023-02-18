pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Execute build steps here
                sh 'make'
            }
        }
        stage('Test') {
            steps {
                // Execute test steps here
                sh 'make test'
            }
        }
        stage('Deploy') {
            steps {
                // Execute deploy steps here
                sh 'make deploy'
            }
        }
    }
    
    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    println 'Pipeline failed'
                }
            }
        }
    }
}
