pipeline {
	agent any
	
	environment {
		MY_TEST_ENV="Hello Env"
		
	}
	
	 stages {
	 	stage('Example stage 1, print Env variable') {
	 		steps {
                 echo "echo ENV ${MY_TEST_ENV}"
                 
                 echo "Jenkins Running build ID ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
	 	}
	 	stage('Stage: Build, Clone code from Github') {
        	steps {
            	sh 'echo "Building the application"'
                // Add commands to build application
                git branch: 'main', url: 'https://github.com/pavankjadda/BookStore.git'
		        script {
		        	def pom = readMavenPom file: 'pom.xml'
		            version = pom.version
		        }
		        sh "mvn install -DskipTests=true"
            }
        }
	 }
}