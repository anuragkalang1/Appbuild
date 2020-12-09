node{
   stage('Hi to Jenkins'){
   
   }
   stage('SCM Checkout'){
     git 'https://github.com/sivajavatechie/JenkinsWar.git'
   }
   stage('Compile-Package-create-war-file'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      bat "${mvnHome}/bin/mvn package"
      }
}
