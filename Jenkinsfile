
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
                    sh "mvn install"
                }
            }
            stage ('Maven Package') {
            steps {
                sh "mvn package"
            }
        }

        stage ('Maven Test') {
            steps { 
                echo "=====================Maven Test========================"
            }
        }
    }

}
