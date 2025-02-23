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
        stage('build code') {
            steps {
                sh 'mvn validate'
            }
        }
    }
}