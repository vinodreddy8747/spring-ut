pipeline{
	agent any
	
	stages{
		stage(‘Compile Stage’){
			steps{
				withMaven(maven : ‘maven_3_5_3’) {
					sh ‘mvn clean install’
				}
			}
		}

		stage(‘Testing Stage’){
			steps{
				withMaven(maven : ‘maven_3_5_3’) {
					sh ‘mvn test’
				}
			}
		}

		stage(‘Deployment Stage’){
			steps{
				withMaven(maven : ‘maven_3_5_3’) {
					sh ‘mvn deploy’
				}
			}
		}


	}
}
