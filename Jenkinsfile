pipeline {
    agent any
    
    tools {
        maven 'mymaven' // Ensure this matches the Maven installation name configured in Jenkins
    }
    stages {
        stage('Clone repo') {
            steps {
                git 'https://github.com/Akshaypython245/DevOpsClassCodes.git'
            }
        }
        stage('Compile') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('Code Review') {
            steps {
                bat 'mvn pmd:pmd'
            }
        }
        stage('Unit Testing') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Code Coverage') {
            steps {
                bat 'mvn verify'
            }
        }
        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
