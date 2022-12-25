
pipeline {
    agent any


    stages {
            stage ('Build No') {
                    steps {
                        sh "echo 'build No. - $BUILD_NUMBER'"
                    }
                }
            stage ('Maven Install') {
                steps {
                    sh "/opt/maven/apache-maven-3.8.6/bin/mvn clean install"
                }
            }
//             stage ('Maven Package') {
//             steps {
//                 sh "/opt/maven/apache-maven-3.8.6/bin/mvn deploy -s settings.xml"
//             }
//         }

        stage ('Code Quality') {
            steps { 
                withSonarQubeEnv(SonarQube Server){
                sh "/opt/maven/apache-maven-3.8.6/bin/mvn sonar:sonar"
                }
            }
        }
    }

}
