pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo '[INFO] Cloning Repository'
               // sh 'git clone --depth 1 --single-branch https://github.com/SparrowNado/demo-website' // template html
                //sh 'ls sparrownado'
            }
        }
        stage('Provision AWS Instance') {
            steps {
                echo '[INFO] Deploying to AWS'
                // sh 'scp -r web_app user@ip_add:/var/www/html'
            }
        }
        stage('Deploy') {
            steps {
                echo 'About to commence Slack Notification Protocol'
                // sh 'sh notif.sh'
            }
        }
        stage('Notification') {
            steps {
                echo '[INFO] Sending Notifications'
                //slackSend channel: '#random', message: 'test', teamDomain: 'randomresearchinc.slack.com', tokenCredentialId: 'slack'
                cleanWs()
            }
        }
    }
}
