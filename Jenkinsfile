pipeline {
    agent any

    stages {
        stage('Maven Build') {
           steps {
                sh "mvn clean package"
            }
        }
        
        stage('Docker-Build') {
            steps {
                sh "docker build -t mohan99061/hiring1:0.0.2 ."
            }
        }
        stage('Docker push') {
           steps {
                sh "docker login -u mohan99061 -p xxxxxx"
               sh "docker push mohan99061/hiring1:0.0.2"
            }
        }
    }
}
