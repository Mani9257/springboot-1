pipeline {
    agent any
    stages
    {
     stage('SCM Checkout')
	    {
                git branch: 'master', url: 'https://github.com/Mani9257/springboot-1.git'
		}    
    
        stage('build')
	{
            sh "${MAVEN-HOME}/bin/mvn clean package -Dmaven.test.skip=true"
		}
    }
}
            
