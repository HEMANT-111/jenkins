pipeline{
	agent {
		node {
			label "dev-H"
			customWorkspace "/mnt/docker/q1"
		}
	}	
		stages {
			stage ('create container') {
				steps {
					/*sh "sudo docker stop container31"*/
					sh  "sudo docker kill container73"
					sh "sudo docker rm container73"
				sh "sudo docker run --name container73 -itdp 70:80 httpd"
				
				}
			}
			stage ('deploy index') {
				steps {
					sh "sudo chmod -R 777 index.html"
					sh "sudo docker cp index.html container73:/usr/local/apache2/htdocs"
					
				}	
			}
				
		
		}
}
