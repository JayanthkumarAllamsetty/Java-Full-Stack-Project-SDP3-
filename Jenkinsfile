node{
  stage('SCM Checkout'){
    git branch:'main',url: 'https://github.com/JayanthkumarAllamsetty/Java-Full-Stack-Project-SDP3-.git'
  }
  stage('Compile-Package'){
    def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Build') {
  steps {
    sh 'mvn clean install'
  }
}

}
