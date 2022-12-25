
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
            stage ('Maven Package : Artifact Upload') {
            steps {
                sh "/opt/maven/apache-maven-3.8.6/bin/mvn deploy -s settings.xml"
            }
        }

        stage ('Maven Test') {
            steps { 
                echo "=====================Maven Test & EMAIL Notification ======================="
                mail body: 'Jenkins Job  - $BUILD_NAME', cc: 'naresh.masurkar1@gmail.com', from: 'naresh.masurkar1@gmail.com', subject: 'Jenkins Job - $BUILD_NUMBER', to: 'naresh170690@rediffmail.com'
            }
        }
    }

}
