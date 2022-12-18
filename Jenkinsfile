
pipeline {
    agent any
    environment {
        maven = "C:\apache-maven-3.8.6\bin"
    }
    stages {
        stage ('maven Build') {
            steps {
                sh "mvn clean package"
            }
        }

        stage ('Maven Test') {
            steps { 
                echo "maven test"
            }
        }
    }

}
