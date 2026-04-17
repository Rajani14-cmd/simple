pipeline {     agent any
    tools {         maven 'maven'
        jdk 'jdk'
    }     stages {
        stage('Checkout') {             steps {
                git branch: 'main', url: 'https://github.com/Rajani14-cmd/simple.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Run') {             steps {
                bat 'java -jar target/sample-maven-app-1.0-SNAPSHOT.jar'
            }
        }
    }
}
