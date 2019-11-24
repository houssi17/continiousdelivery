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
                sh 'sudo mvn package'
            }
        }
    

    
        stage('creating docker image locally') {
            steps {
                sh 'sudo mvn dockerfile:build'
            }
        }
    
   }
}
