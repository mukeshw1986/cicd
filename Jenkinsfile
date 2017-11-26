pipeline {
	agent any

	stages {
	 	stage ('compile stage') {

	 		steps { 
	 			withmaven(maven : 'maven_3_5_2') {
	 				sh 'mvn clean compile	'
	 		  	}
	 		}
		}

		stage ('testing stage'){

			steps { 
	 			withmaven(maven : 'maven_3_5_2') {
	 				sh 'mvn test'
	 		  	}
	 		}
		}

		stage ('Deployment stage'){

			steps { 
	 			withmaven(maven : 'maven_3_5_2') {
	 				sh 'mvn deploy'
	 		  	}
	 		}
		}
	}	
}
