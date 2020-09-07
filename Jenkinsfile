pipeline{
    agent any
    stages{
        stage("SCM checkout"){
            steps{
                git 'https://github.com/pusa9/spring-petclinic.git'
            }
        }
            stage("Maven Build"){
            steps{
                sh "mvn clean package"
            }
            }
        
    }
}
