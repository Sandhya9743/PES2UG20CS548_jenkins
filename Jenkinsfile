pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o CS548-1 origin/main/hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './CS543-1'
            }
        }
        
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
