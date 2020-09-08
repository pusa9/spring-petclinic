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
			
                stage('Upload to nexus'){
					steps{
					
						nexusArtifactUploader artifacts: [[artifactId: 'spring-petclinic', classifier: '', 
                                                                                   file: 'target/petclinic-2.1.0.war', type: 'war']],
                                                        credentialsId: 'nexus3',
                                                        groupId: 'org.springframework.boot',
                                                        nexusUrl: '172.31.2.179:8081', 
                                                        nexusVersion: 'nexus3', 
                                                        protocol: 'http', 
                                                        repository: 'venkat', 
                                                        version: '2.1.0'
					}
				
				}
			}
}
