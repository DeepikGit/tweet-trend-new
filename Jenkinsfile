
pipeline {
    agent {
        node {
            label 'maven-slave'
        }
    }
environment {
    path="/opt/apache-maven-3.9.9/bin:$PATH"
    IMAGE_NAME = "my-local-app"
    IMAGE_TAG = "latest"
    WORKSPACE = "${WORKSPACE}/jarstaging/com/valaxy/demo-workshop/2.1.2/demo-workshop-2.1.2.jar"
}
    stages {
        stage('package code') {
            steps {
                sh 'mvn clean deploy -Dmaven.test.skip=true'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh """
                        docker build --build-arg JAR_FILE=$WORKSPACE -t $IMAGE_NAME:$IMAGE_TAG .
                    """
                }
            }
        }
        stage('deploy Docker Image') {
            steps {
                script {
<<<<<<< HEAD
                    sh './myscript1.sh'
=======
                    sh './myscript.sh'
>>>>>>> 6eb5886694b3a9d399b5588dd3cee2608d6c11d6
                }
            }
        }


    }

}
