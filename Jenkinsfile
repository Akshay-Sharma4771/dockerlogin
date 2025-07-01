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
					sh 'sudo docker build -t tomcat-repo1:$LATEST_TAG .'
					sh 'sudo docker tag tomcat-repo1:$LATEST_TAG akshay741/dockpipe'
				      }
				}
		}	
}
		

