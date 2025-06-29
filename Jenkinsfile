pipeline {
       agent any
	   stages {
	          stage("structure") {
			        	steps {
						git branch: 'main', url: 'https://github.com/Akshay-Sharma4771/dockerlogin.git'
							}
						}
			  stage("build") {
			        steps {
					       sh 'sudo mvn clean package'
						   }
						}
			  stage("test") {
			        steps {
					       sh 'sudo java -jar target/*.jar >  /var/lib/jenkins/workspace/mav/text.txt'
						   }
						}
		}	
}				

