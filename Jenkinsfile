pipeline {
    agent{
	    label'slave-lab'
    }
    stages {
         stage('Checkout') {
            steps {
                checkout scm
		}
	 }
         stage('Build') {
            steps {
                sh 'JAVA_HOME=/home/redhat/slaved/jdk-11.0.24 /home/redhat/slaved/apache-maven-3.9.9/bin/mvn install'
                }
         }
         stage('Deployment'){
            steps {
                sh 'cp target/Project2.war /home/redhat/slaved/apache-tomcat-9.0.93/webapps'
                }
         }
    	}
    }
