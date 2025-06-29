 pipeline {
       agent any
	   stages {
	          stage("Structure") {
			        steps {
					       git branch: 'main', url: 'https://github.com/Akshay-Sharma4771/dockerlogin.git'
						   }
						}
			  stage("build") {
			        steps {
					       sh 'sudo mvn clean package'
						   }
						}
			  stage("finalize") {
			        steps {
					       sh 'sudo java -jar target/*.jar >/var/lib/jenkins/workspace/maven/text.txt'
						   }
						}
		}	
}
		

