pipeline {
    agent any
    
    tools {
        maven "M398"
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }    
//        stage('git'){
//            steps{
//                git branch: 'main', credentialsId: '5dc34723-30a4-409a-892d-a7fe17f0341b', url: 'https://github.com/samba8514/jenkins-hello-world.git'
//            }
 //       }
        stage('Build'){
            steps{
                sh "mvn clean package -DskipTests=true"
            }
        }
        stage('UnitTest'){
            steps{
                sh "mvn test"
            }
        }
    }
}

