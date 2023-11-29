pipeline {

    agent {
      label {
        label "slave2"
        customWorkspace "/mnt/branch2"
          }
       }

    stages {
      
       stage ("1st") {
          steps {

          sh "sudo yum install httpd -y"
         sh " sudo yum install git -y"
             }
          }

       stage ("2nd") {
              steps {
           git url:"https://github.com/HEMANT-111/jenkins.git", branch:"q2"
                   }
            }

       stage ("3rd") {
              steps {
              sh "sudo cp ./index.html /var/www/html"
              sh "sudo chmod -R 777 /var/www/html"
                    }
               }
        stage ("4th") {
           steps {
            sh "sudo service httpd restart"
                    }
                 }
           }
       }
