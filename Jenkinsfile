ipeline {
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
        stage('Build'){
            steps{
                sh "mvn clean package -DskipTests=true"
            }
        }
        stage('UnitTest') {
            steps {
                script {
                    for (int i = 0; i < 60; i++) {
                    echo "${i + 1}"
                    sleep 1
                }
            }
            sh "mvn test"
        }
    }
}

