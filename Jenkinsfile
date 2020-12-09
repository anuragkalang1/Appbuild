node{
   stage('Hi'){
     runTask()
   }
   stage('SCM Checkout'){
     git 'https://github.com/sivajavatechie/JenkinsWar.git'
   }
   stage('Compile-Package-create-war-file'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh ''' cd /usr/create-war '''
      mvn clean install
      }
}

def runTask()
{
sh '''
  echo "Hello"
  '''
}

