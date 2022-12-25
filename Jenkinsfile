
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
                echo "=====================Maven Test========================"
                mail bcc: '', body: '', cc: 'naresh.masurkar1@gmail.com', from: '', replyTo: '', subject: 'Jenkins Job - ', to: 'naresh170690@rediffmail.com'
            }
        }
    }

}
