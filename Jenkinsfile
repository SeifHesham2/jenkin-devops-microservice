pipeline {
   // agent any
   agent {docker {image 'alpine:latest'}}
   stages {
	  stage('Build') {
		 steps {
		    sh 'alpine --version'
			echo 'Building..'
		 }
	  }
	  stage('Test') {
		 steps {
			echo 'Testing..'
		 }
	  }
	  stage('Deploy') {
		 steps {
			echo 'Deploying....'
		 }
	  }
   } 
   
 post {
	  always {
		 echo 'One way or another, I have finished'
	 success {
		echo 'I succeeded!'
	 }
	 failure {	
		echo 'I failed :('
	 }
	  }
   }

}
