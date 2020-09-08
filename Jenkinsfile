pipeline{
	agent any
	stages{
	
		stage('SCM - Checkout'){
			steps{
				git 'https://github.com/pusa9/spring-petclinic.git'
			
			}
		}
		stage('Maven Build'){
					steps{
					
						sh "mvn clean package"
					}
				
				}
			
			}
}
