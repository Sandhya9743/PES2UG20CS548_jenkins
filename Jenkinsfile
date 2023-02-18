pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
    
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    
    stage('Deploy') {
      steps {
        sh 'scp target/myapp.war user@server:/path/to/deploy'
      }
    }
  }
  
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
