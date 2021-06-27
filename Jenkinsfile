pipeline {
  agent any
  stages {
    stage('sourcecode') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('compile') {
      steps {
        sh 'mvn package'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('report') {
      steps {
        junit 'target/surefire-reports/*.xml'
      }
    }

  }
}