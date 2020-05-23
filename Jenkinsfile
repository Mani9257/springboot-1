pipeline {
    agent any
    stages
        stage('SCM Checkout') {
            steps {
                git branch: 'dev', url: 'https://github.com/Mani9257/springboot-1.git'
            }
        }
        stage('build') {
            steps {
		withSonarQubeEnv('sonar') {
        	        		sh "C:\apache-maven-3.6.2\bin\mvn clean verify sonar:sonar"
		}
            }
        }
       stage("Quality Gate") {
            steps {
              timeout(time: 30, unit: 'SECONDS') {
                waitForQualityGate abortPipeline: true
              }
            }
          }
        stage("Deploy"){
            steps {
                sh "C:\apache-maven-3.6.2\bin\mvn deploy"
            }
        }    
    }
}
