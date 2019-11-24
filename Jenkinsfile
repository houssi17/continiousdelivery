pipeline {
    agent any
    stages {
        stage('cleaning') {
            steps {
                sh 'mvn clean'
            }
        }
    }
    stages {
        stage('packaging') {
            steps {
                sh 'mvn package'
            }
        }
    }

    stages {
        stage('creating docker image locally') {
            steps {
                sh 'mvn dockerfile:build'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
