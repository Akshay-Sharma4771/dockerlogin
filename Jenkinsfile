pipeline {
       agent any

	   stages {
	          stage("Structer") {
			     steps {
				     git branch: 'main', url: 'https://github.com/Akshay-Sharma4771/java.git'
			           }
				}
			  stage("testing") {
			        steps {
					sh 'sudo mvn clean package'
				      }
				}
			  stage("image-built") {
			        steps {
					sh 'sudo docker build -t tom-repo:$build_tag .'
					sh 'sudo docker tag tom-repo:$build_tag akshay741/dockerpipe
				      }
				}
		}	
}
		

