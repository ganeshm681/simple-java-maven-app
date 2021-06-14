node{
   stage 'checkout'
          checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'cdad465b-1d65-4b41-bce7-da95a887c7f4', url: 'https://github.com/ganeshm681/simple-java-maven-app.git']]])
def mvnHome= tool 'M2'
   stage 'build'
   sh '\'${mvnHome}/bin/mvn -B -DskipTests clean package\''
}
