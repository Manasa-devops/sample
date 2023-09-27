pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
               checkout([$class: 'GitSCM', branches: [[name: master], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [] url:'https://github.com/Manasa-devops/sample.git']])
            }
        }        stage('Build') {
            steps {
                // Build the Maven project
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                // Add deployment steps here (e.g., deploy to a server)
                sh 'echo "Deployment step"'
            }
        }                                                                                                                                                                   
    }
}
