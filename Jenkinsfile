pipeline {
       agent any

	   stages {
	          stage("structure") {
			        steps {
					git branch: 'main', url:'https://github.com/Akshay-Sharma4771/java.git'
					}
					}
			  stage("test") {
			        steps {
					sh 'sudo mvn clean package'
					}
					}
			  stage("img-build") {
			        steps {
					sh 'sudo docker build -t tom-repo:$LAST_TAG .'
					sh 'sudo docker tag tom-repo:$LAST_TAG akshay741/dockin:$LAST_TAG'
					}
					}
		}	
}
