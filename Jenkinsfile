pipeline {
  agent any
  stages {
    stage('pull') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'ba80fea2-6746-43f0-8a9f-8f4fca2db48b', url: 'git@github.com:cwww3/jenkins.git']]])
      }
    }

    stage('build') {
      steps {
        sh 'go build main.go'
      }
    }

    stage('run') {
      steps {
        sh './main'
      }
    }

  }
  tools {
    go 'localGo'
  }
}