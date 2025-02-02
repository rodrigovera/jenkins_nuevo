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
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Build"
				
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
