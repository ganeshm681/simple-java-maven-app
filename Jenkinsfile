node{
      
    echo "checkout code from github account"
   stage 'checkout'
          def BRANCH= env.BRANCH_NAME
	  echo "branch is ${BRANCH}"
          checkout([$class: 'GitSCM', branches: [[name: '*/${env.BRANCH_NAME}']], extensions: [], userRemoteConfigs: [[credentialsId: 'cdad465b-1d65-4b41-bce7-da95a887c7f4', url: 'https://github.com/ganeshm681/simple-java-maven-app.git']]])
echo "build starts"
   
   def mvnHome = tool 'Maven 3'
   stage 'build'
   sh "${mvnHome}/bin/mvn -B -DskipTests clean package"

echo "build completed"

}
