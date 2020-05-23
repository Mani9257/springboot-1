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
        	$ cmd.exe /C "C:\apache-maven-3.6.2\bin\mvn.cmd clean install sonar:sonar && exit %%ERRORLEVEL%%"
		}
            }
}
}
}
