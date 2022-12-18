
pipeline {
    agent any
    stages {
        stage ('Git Checkout') {
            steps {
                git 'https://github.com/naresh170690/ion-web-app.git'

            }
        }
        stage ('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        
    }


}
