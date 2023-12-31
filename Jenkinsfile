pipeline{
	agent {
		node {
			label "built-in"
			customWorkspace "/mnt/docker/q1"
		}
	}	
		stages {
			stage ('create container') {
				steps {
					
					/*sh  "sudo docker kill container73"
					sh "sudo docker rm container73"*/
				/*sh " docker run --name kanu -itdp 70:80 httpd"*/
				sh " docker run --name sinu -itdp 71:80 httpd"
				sh " docker run --name sinu1 -itdp 72:80 httpd"
					
				}
			}
			stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html sinu:/usr/local/apache2/htdocs"
					sh "docker cp index.html sinu1:/usr/local/apache2/htdocs"
					
					
				}	
			}
				
		
		}
}
