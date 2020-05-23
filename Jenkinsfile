node{
      stage('Checkout'){
         git 'https://https://github.com/Mani9257/springboot-1.git'
       }  
      stage('Build'){
         //// Get maven home path and build
            def mvnHome = tool name: 'MAVEN-HOME', type: 'maven' 
        sh "${mvnHome}/bin/mvn clean package"
      }
}
            
