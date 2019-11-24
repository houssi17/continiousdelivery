pipeline {
    agent any
    stages {
        stage('cleaning') {
            steps {
                sh 'mvn clean'
            }
        }
    }
    
        stage('packaging') {
            steps {
                sh 'mvn package'
            }
        }
    

    
        stage('creating docker image locally') {
            steps {
                sh 'mvn dockerfile:build'
            }
        }
    
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
