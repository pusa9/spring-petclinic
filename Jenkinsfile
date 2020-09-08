pipeline{
	agent any
	stages{
	
		stage('SCM - Checkout'){
			steps{
				git url: 'https://github.com/javahometech/myweb'
			
			}
		}
		stage('Maven Build'){
					steps{
					
						sh "mvn clean package"
					}
				
				}
			
			}
}
