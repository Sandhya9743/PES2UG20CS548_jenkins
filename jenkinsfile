pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o try.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                sh './try.cpp'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
