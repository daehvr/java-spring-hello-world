pipeline {
	agent any
	
	environment {
		MY_TEST_ENV="Hello Env"
		
	}
	
	 stages {
	 	stage('Example stage 1, print Env variable') {
	 		steps {
                 echo "echo ENV ${MY_TEST_ENV}"
                 
                 echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
	 	}
	 }
}