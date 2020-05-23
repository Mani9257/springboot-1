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
        	 sh "${MAVEN-HOME}/bin/mvn clean package -Dmaven.test.skip=true"
		}
            }
}
}
}
