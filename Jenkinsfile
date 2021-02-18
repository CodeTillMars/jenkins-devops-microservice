//Scripted Pipeline approach
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Integration Test"
// 	}
// }

//Declarative

pipeline {	
	//agent any
	agent { docker {image 'maven:3.6-ibmjava'}}

	stages{
		stage('Build'){
		steps{
			sh "mvn --version"
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
	post{
		always {
		echo 'I am awesome. I run Always'	

		}
		success{
			echo 'I run  when you  are successful'
		}
		failure{
			echo 'I run when you are not successful'
		}


	}
	
}