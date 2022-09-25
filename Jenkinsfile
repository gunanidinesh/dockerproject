#!groovy

pipeline{
	agent none
  stages {
  	stage('Maven Install') {
    	agent {
      	docker {
        	image 'maven:3.5.0'
        }
      }
      steps {
      	sh 'mvn clean install'
      }
    }
    stage('Docker Build') {
    	agent any
      steps {
      	sh 'docker build -t dmgunani/newdockimg.'
      }
    }
  }
}


cat /home/gunanidineshgma/docker_project/dockerproject/index.html
