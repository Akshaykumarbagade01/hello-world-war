pipeline {
  agent {label "slave_server1"}
      stages {
           stage ("tomcat buid") {
              steps {
                      sh 'mvn package'
		      sh 'ls'
	      }
	   }
	   stage ("tomcat diploy")  {
              steps {
                      sh 'sudo cp -R target/hello-world-war-1.0.0.war /opt/tomcat/webapps/'
                      sh 'sudo sh /opt/tomcat/webapps/bin/shutdown.sh'                   
                      sh 'sleep 3'
                      sh 'sudo sh /opt/tomcat/webapps/bin/startup.sh'
                      echo "diployment is sucessfull"
                      echo "copy the public ip of instace and open it in browser with port:8090"
	      }
	   }	      
      }
}
