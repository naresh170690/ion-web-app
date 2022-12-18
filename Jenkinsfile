
pipeline {
    agent any

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
