pipeline {
  agent {label "slave_server1"}
      stages {
           stage ("tomcat buid") {
              steps {
                      sh 'mvn package'
		      sh 'ls'
	      }
	   }
      }
}
