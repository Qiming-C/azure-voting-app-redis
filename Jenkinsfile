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
            sh '''#!/bin/bash
                cd azure-vote/
                docker images -a
                docker build -t jenkins-pipeline .
                cd ..
                '''
          }
        }
    }
}