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
        git add .
        git commit -m "Pushing the generated target (war file) to the remote repo"
        git push origin master
        mvn clean install
        '''
      }
   stage('Configure/Deploy-Ansible'){
      sh ''' ansible-playbook warDeploy.yml '''
   }
}


