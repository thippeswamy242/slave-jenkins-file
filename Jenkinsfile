pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                checkout scm
                sh 'hostname -i'
                 
            }
        }
        stage('Test on Linux') {
            agent { 
                label 'slave-1'
            }
            steps {
                sh 'sudo mkdir /root/demo'
            
            }
        }
        
    }
    
}
