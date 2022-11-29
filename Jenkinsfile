pipeline {
	agent none
        stages {
           stage ("tomcat buid") {
	       agent {label "slave_server1"}
              steps {
                      sh 'mvn package'
		      sh 'ls'
	      }
	   }
        }
}
