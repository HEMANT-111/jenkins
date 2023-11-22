pipeline {
    agent {
        label {
            label "slave-1"
            customWorkspace "/mnt/hsk/"
        }
    }

    stages {
        
        stage("1") {
            
            steps {
                sh "yum install httpd -y"
            }
        }
       
        
        
        stage ("2") {
           
            steps {
                
            sh"#!/bin/bash"
            sh "echo 'hello' > index.html"
            sh "cp /mnt/hsk/index.html /var/www/html"
            sh "chmod -R 777 /var/www/html/"
        }
    }
    
    stage("4") {
            
            steps {
                sh "service httpd restart"
            }
      }
   }
}
