pipeline {
    agent any

    environment {
        mvnHome = tool 'Maven' // Define the Maven installation to use
        gitRepo = 'https://github.com/JayanthkumarAllamsetty/Java-Full-Stack-Project-SDP3-.git' // Replace with your GitHub repository URL
        gitBranch = 'main' // Replace with the branch you want to build
    }

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: gitBranch]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: gitRepo]]])
            }
        }

        stage('Build project') {
            steps {
                sh '/path/to/maven/bin/mvn clean package'
 // Run Maven to build the project
            }
        }
    }
}
