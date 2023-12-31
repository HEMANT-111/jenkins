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
				sh " docker run --name kanu -itdp 70:80 httpd"
					
				}
			}
			stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html kanu:/usr/local/apache2/htdocs"
					
					
				}	
			}
				
		
		}
}
