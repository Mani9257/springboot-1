node{
      def tool name: 'MAVEN-HOME', type: 'maven' 
      stage('Checkout'){
         git 'https://https://github.com/Mani9257/springboot-1.git'
       
      }  
      stage('Build'){
         //// Get maven home path and build
        sh "${MAVEN-HOME}/bin/mvn clean package -Dmaven.test.skip=true"
      }
}
            
