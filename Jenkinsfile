pipeline {
    agent {
        node {
            label 'maven-slave'
        }
    }

    stages {
        stage('clone the code') {
            steps {
                git branch: 'main', credentialsId: 'Maven-server-cred', url: 'https://github.com/DeepikGit/tweet-trend-new.git'
            }
        }
    }
}