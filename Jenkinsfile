pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Echo Version'){
            steps{
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        
        
        stage('Build'){
            steps{
                //git branch: 'main', changelog: false, poll: false, url: 'https://github.com/sidd-harth/jenkins-hello-world.git'
                //git branch: 'main', changelog: false, poll: false, url: 'https://github.com/thegodsson/jenkins-hello-world.git'
                sh "mvn clean package -DskipTests=true"
            }
        }
        
         stage('Unit Test'){
            steps{
               sh "mvn test"
            }
        }
		
        
    }
}
