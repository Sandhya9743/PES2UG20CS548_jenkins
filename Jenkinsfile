pipeline {
    agent any 
    stages {
        stage ('Build') {
            steps {
                sh 'g++ -o PES2UG20CS548-1 hello.cpp'
            }
        }
        stage ('Test') {
            steps {
                sh './PES2UG20CS548-1'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
