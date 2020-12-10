node{
   stage('SCM Checkout'){
     git '' //replace your githib url within the quotes
   }
   stage('Compile-Package-create-war-file'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh ''' 
        echo "$PWD"
        mvn validate
        mvn compile
        mvn test
        mvn package
        '''
      }
   stage('Configure/Deploy-Ansible'){
      sh ''' ansible-playbook warDeploy.yml '''
   }
}


