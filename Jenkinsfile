pipeline {
    agent any
    stages {
        stage('clean') {
            steps {
                sh 'mvn clean'
            }
        }
    
    
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    

    
        stage('creating docker image locally') {
            steps {
                sh 'mvn dockerfile:build'
            }
        }
    
   }
}
