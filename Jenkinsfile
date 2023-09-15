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
            sh '''
                    cd azure-vote
                    ls
                    docker images -a
                    docker build -t jenkins-pipeline .
                '''
          }
        }
    }
}