pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/jaisaiveera/Petclinic.git'
            }
        }
        
        stage('Compile') {
            steps {
               sh "mvn clean compile"
            }
        }
        
        stage('Build') {
            steps {
               sh "mvn clean package -DskipTests=true"
            }
        }
        
        
        
        
    }
}
