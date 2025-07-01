pipeline {
       agent any

           stages {
                  sitage("Structure") {
                             steps {
                                     git branch: 'main', url: 'https://github.com/Akshay-Sharma4771/dockerlogin.git'
                                   }
                                }
                          stage("testing") {
                                steps {
                                        sh 'sudo mvn clean package'
                                      }
                                }
                          stage("image-built") {
                                steps {
                                        sh 'sudo docker build -t tomcat-re:$LAT_TAG .'
                                        sh 'sudo docker tag tomcat-re:$LAT_TAG akshay741/dockpipe'
                                      }
                                }
                }
}
