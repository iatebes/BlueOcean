pipeline {
  agent any
  stages {
    stage('Collect source') {
      parallel {
        stage('Collect') {
          steps {
            git(url: 'https://github.com/iatebes/MathApi.git', branch: 'master')
          }
        }
        stage('Change config') {
          steps {
            sh '''ls -la
pwd'''
          }
        }
      }
    }
    stage('Build mvn') {
      steps {
        sh 'mvn package'
      }
    }
    stage('Deploy tomcat') {
      steps {
        sh 'whoami'
      }
    }
  }
}