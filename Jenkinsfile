pipeline {

    agent {
      label {
        label "slave3"
        customWorkspace "/mnt/branche"
          }
       }

    stages {
      
       stage ("1st") {
          steps {

          sh "yum install httpd -y"
             }
          }

       stage ("2nd") {
              steps {
           git url:"https://github.com/HEMANT-111/jenkins.git", branch:"q3"
                   }
            }

       stage ("3rd") {
              steps {
              sh "cp ./index.html /var/www/html"
              sh "chmod -R 777 /var/www/html"
                    }
               }
        stage ("4th") {
           steps {
            sh "service httpd restart"
                    }
                 }
           }
       }
