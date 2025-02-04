//node {
//	stage('Build') {
//		echo "Build"
//	}
//	stage('Test') {
//		echo "Test"
//	}
//	stage('Integration Test') {
//		echo "Test"
//	}
//}
pipeline{
	//agent any
	
	agent{docker{ image 'maven:3.8.8-eclipse-temurin-17' } }
	environment {
		mavenHome= tool 'myMaven'
		dockerHome= tool 'mydocker'
		PATH= "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
				
			}
		}
	stage('Test'){
			steps{
				
				echo "Test"
				
			}
		}
	stage('Integration Test'){
			steps{
				
				echo "Integration Test"
			}
		}
	}
	post {
		always{
			echo 'im awesome. i run always'
		}
		success{
			echo 'im run when you are successful'
		}
		failure{
			echo 'i run when you fail'
		}
	}
}
