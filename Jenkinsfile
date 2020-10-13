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
                sh 'sudo rm -rf  /opt/*' 
                sh 'sudo mkdir /opt/swamy'
                sh 'hostname -i'
            }
        }
        
        stage('Test on Slave-2') {
            agent { 
                label 'slave-2'
            }
            steps {
                sh 'sudo rm -rf /root/demo/*'
                sh 'sudo mkdir /root/demo/swamy'
                sh 'hostname -i'
            
            }
        }
    }
    
}
