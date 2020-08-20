pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
        jdk 'JDK 8'
    }
    stages {
        stage('Build') {
            steps {
                echo 'maven clean'
                //ABC indicates the folder name where the pom.xml file resides.
                bat ' mvn -f pom.xml clean install'  
            }
            post {
                success {
                    echo 'Now Archiving'
                }
            }
        }
    }
}
