node{
   stage('Hi'){
     runTask()
   }
   stage('SCM Checkout'){
     git 'https://github.com/anuragkalang1/Appbuild.git'
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
}

def runTask()
{
sh '''
  echo "Hello"
  '''
}

