pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
            post{
                success {
                    mail to: "joshualbourquin@gmail.com",
                    subject: "Test Status Email - Success",
                    body: "Test ran successfully."
                }
                unsuccessful {
                    mail to: "joshualbourquin@gmail.com",
                    subject: "Test Status Email - Unsuccessful",
                    body: "Test ran unsuccessfully."
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Code Analysis'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Security Scan'
            }
            post{
                success {
                    mail to: "joshualbourquin@gmail.com",
                    subject: "Security Scan Status Email - Success",
                    body: "Security Scan ran successfully."
                }
                unsuccessful {
                    mail to: "joshualbourquin@gmail.com",
                    subject: "Security Scan Status Email - Unsuccessful",
                    body: "Security Scan ran unsuccessfully."
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
                echo 'Integration Tests on Staging'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production'
            }
        }
    }
}
