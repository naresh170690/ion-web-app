
pipeline {
    agent any
    environment {
        PATH = "/c/apache-maven-3.8.6/bin:$Path "
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
