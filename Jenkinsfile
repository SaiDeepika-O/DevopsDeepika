pipeline {
    agent any

    tools {
        jdk 'jdk8'         // Must match Jenkins -> Global Tools -> JDK name
        maven 'maven3'     // Must match Jenkins -> Global Tools -> Maven name
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/SaiDeepika-O/DevopsDeepika.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

    }
}
