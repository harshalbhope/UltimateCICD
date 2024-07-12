/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent {
        docker {
            image 'harshalb/maven-harshalb-docker-agent:v1'
            args '--user root -v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                sh 'echo passed'
            }
        }
        stage('Build and Test') {
            steps {
                sh 'ls -ltr'
                sh 'cd spring-boot-app && mvn clean package'
            }
        }
    }
}
