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
                sh 'sudo mkdir /root/swamy-2'
                sh 'sudo cat hellofrom jenkins >> /root/demo.txt'
                sh 'hostname -i'
                sh 'sudo rm -rf /root/demo4'
                sh 'sudo rm -rf /root/demo1'
            
            }
        }
        
        stage('Test on Slave-2') {
            agent { 
                label 'slave-2'
            }
            steps {
                sh 'sudo mkdir /root/swamy-2'
                sh 'hostname -i'
            
            }
        }
    }
    
}
