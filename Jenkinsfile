pipeline {

    agent {
      label {
        label "built-in"
        customWorkspace "/mnt/branch1"
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
           git 
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

