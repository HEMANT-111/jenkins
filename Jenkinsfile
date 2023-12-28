pipeline{
	agent {
		node {
			label "built-in"
			customWorkspace "/mnt/docker/q2"
		}
	}	
		stages {
			stage ('create container') {
				steps {
					sh  "docker kill container2"
					sh "docker rm container2"
				sh "docker run --name container2 -itdp 100:80 httpd"
				
				}
			}
			stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container2:/usr/local/apache2/htdocs"
					
				}	
			}
				
		
		}
}
