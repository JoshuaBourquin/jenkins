pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build - Possible tool: Maven'
            }
        }
        stage('Test') {
            steps {
                echo 'Test - Possible tool: JUnit'
            }
            post{
                success {
                    emailext to: "joshualbourquin@gmail.com",
                    subject: "Test Status Email - Success",
                    body: "Test ran successfully.",
                    attachLog: true
                }
                unsuccessful {
                    emailext to: "joshualbourquin@gmail.com",
                    subject: "Test Status Email - Unsuccessful",
                    body: "Test ran unsuccessfully.",
                    attachLog: true
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Code Analysis - Possible tool: Raxis'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Security Scan - Possible tool: ZAP'
            }
            post{
                success {
                    emailext to: "joshualbourquin@gmail.com",
                    subject: "Security Scan Status Email - Success",
                    body: "Security Scan ran successfully.",
                    attachLog: true
                }
                unsuccessful {
                    emailext to: "joshualbourquin@gmail.com",
                    subject: "Security Scan Status Email - Unsuccessful",
                    body: "Security Scan ran unsuccessfully.",
                    attachLog: true
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration Tests on Staging - Possible tool: Testsigma'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production'
            }
        }
    }
}
