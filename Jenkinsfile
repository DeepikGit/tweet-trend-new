pipeline {
    agent {
        node {
            label 'maven-slave'
        }
    }
environment {
    path="/opt/apache-maven-3.9.9/bin:$PATH"
}
    stages {
        stage('package code') {
            steps {
                sh 'mvn clean deploy' 
            }
        }
    }
}