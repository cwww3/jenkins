pipeline {
    agent any
    
    tools {
        go 'localGo'
    }
    
    stages {
//         stage('pull') {
//             steps {
//                 checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'aa448fff-be31-4df0-8e0a-723987b11997', url: 'https://github.com/cwww3/jenkins.git']]])
//             }
//         }
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
}
