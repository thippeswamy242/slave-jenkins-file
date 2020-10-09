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
        stage('Test on Slave-1') {
            agent { 
                label 'slave-1'
            }
            steps {
                sh 'sudo mkdir /root/demo4'
                sh 'hostname -i'
                sh 'sudo rm -rf /root/demo'
                sh 'sudo rm -rf /root/demo1'
            
            }
        }
        
        stage('Test on Slave-2') {
            agent { 
                label 'slave-2'
            }
            steps {
                sh 'sudo mkdir /root/demo'
                sh 'hostname -i'
            
            }
        }
    }
    
}
