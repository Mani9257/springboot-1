node{
      stage('Checkout'){
         git 'https://github.com/Mani9257/springboot-1'
       }  
      stage('Build'){
         //// Get maven home path and build
            //// def mvnHome = tool name: 'MAVEN-HOME', type: 'maven' 
        bat "C:\apache-maven-3.6.2\bin\mvn clean install"
      }
}
            
