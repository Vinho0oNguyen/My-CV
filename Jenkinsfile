pipeline{
    agent any
    stages{
        stage('Git clone'){
            steps{
                git branch: 'main', credentialsId: '5ecb6610-fa67-4c23-9ce4-85772582a569', url: 'https://github.com/Vinho0oNguyen/My-CV.git'
            }
            
        }
        
        stage('Build'){
            steps{
                sh '''#!/bin/bash
                    ssh -T -i /home/jenkins/web-server.pem user1@192.168.1.95 << EOF
                    cd /var/www/html
                    rm .git/refs/remotes/origin/main
                    git pull'''
            }
        }
        
            
    }
}
