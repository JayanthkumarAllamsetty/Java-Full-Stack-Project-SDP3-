pipeline {
    agent any

    environment {
        mvnHome = tool name: 'MAVEN', type: 'maven' // Define the Maven installation to use
        gitRepo = 'https://github.com/JayanthkumarAllamsetty/Java-Full-Stack-Project-SDP3-.git' // Replace with your GitHub repository URL
        gitBranch = 'main' // Replace with the branch you want to build
        PATH="${mvnHome}/bin:${PATH}" // Add Maven bin directory to PATH
    }

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: gitBranch]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: gitRepo]]])
            }
        }

        stage('Build project') {
            steps {
                bat 'mvn clean package' // Run Maven to build the project
            }
        }
    }
}
