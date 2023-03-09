#!groovy
pipeline {
	agent {
		docker {image 'maven:3.5.0'}
	}
	stages {
		stage('maven-build') {
			steps {
				sh 'mvn clean install'
			}
		}
	}
}
