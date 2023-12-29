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
					/*sh  "docker kill container1"
					sh "docker rm container1"*/
				sh "sudo docker run --name container1 -itdp 70:80 httpd"
				
				}
			}
			stage ('deploy index') {
				steps {
					sh "sudo chmod -R 444 index.html"
					sh "sudo docker cp index.html container1:/usr/local/apache2/htdocs"
					
				}	
			}
				
		
		}
}
