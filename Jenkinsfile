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
        	 sh "C:\apache-maven-3.6.2\bin\mvn mvn clean install"
		}
            }
}
}
}
