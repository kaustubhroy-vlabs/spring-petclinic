#!groovy
pipeline {
	agent {
		docker {image 'maven:3.5.0'}
	}
	stages {
                stage("Docker Build") {
                        agent any
                        steps {
                                sh 'docker build -t demo/spring-petclinic:latest.'
                        }
                        
                }
		stage('maven-build') {
			steps {
				sh 'mvn clean install'
			}
		}
	}
}
