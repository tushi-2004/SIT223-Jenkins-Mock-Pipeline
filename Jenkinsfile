pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build Stage: Building and packaging the application using Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Testing Stage: Running unit tests using JUnit and integration tests using Selenium.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis Stage: Analysing code quality using SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security Scan Stage: Scanning vulnerabilities using OWASP Dependency-Check.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging Stage: Deploying application to AWS EC2 staging server.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Staging Test Stage: Running integration tests on staging using Postman/Newman.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production Stage: Deploying final application to AWS EC2 production server.'
            }
        }
    }
}
