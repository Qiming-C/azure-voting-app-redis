pipeline {
    agent any
    
    stages {
        stage('Verify Branch') {
            steps {
                echo "${GIT_BRANCH}"
            }
        }
        stage('Build docker') {
          steps {
            sh 'cd azure-vote/'
            sh 'docker images -a'
            sh 'docker build -t jenkins-pipeline .'
          }
        }
    }
}