pipeline {
    agent any
    stages {
         stage('Checkout') {
            steps {
                checkout scm
		}
	 }
         stage('Build') {
            steps {
                sh 'mvn install'
                }
         }
         stage('Deployment'){
            steps {
                sh 'cp target/Project1.war /home/chaitanya/Documents/Devops-Tool/apache-tomcat-9.0.93/webapps'
                }
         }
    	}
    }
