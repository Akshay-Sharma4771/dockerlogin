pipeline {
       agent any
	   stages {
	          stage("structure") {
			        steps {
					git branch: 'main', url: 'https://github.com/Akshay-Sharma4771/java.git'
					}
					}
			  stage("test") {
			        steps {
					sh 'sudo mvn clean package'
					}
					}
			  stage("img-build") {
			        steps {
					sh 'sudo docker build -t tomcat-repo:$LAT_TAG .'
					sh 'sudo docker tag tomcat-repo:$LAT_TAG akshay741/dockin'
					}
					}
		}	
}
