pipeline {
    agent any
    stages
    {
     stage('SCM Checkout')
	    {
            steps 
		{
                git branch: 'master', url: 'https://github.com/Mani9257/springboot-1.git'
		}    
    }
        stage('build') {
            steps {
		withSonarQubeEnv('sonar') 
		    {
        	sh "${mvnHome}/bin/mvn clean install"
		}
            }
}
}
}
