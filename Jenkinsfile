
pipeline {
    agent any
    // enviroment {

    // }
    stages {
        stage ('maven Build') {
            steps {
                sh "mvn clean package"

            }
        }
        stage ('Maven test'){
            stpes { 
                echo "maven test"
            }
        }
    }

}
