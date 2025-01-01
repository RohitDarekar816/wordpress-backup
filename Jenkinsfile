@Library('Shared')_
pipeline {
    agent any
    stages {
        stage('Download files from ftp') {
            steps{
                 sh 'apt-get update'
                 sh 'apt-get install -y lftp curl'
                 sh 'apt-get install -y rclone'
                 sh 'echo \"Logging into FTP server\"'
                 sh 'lftp -u admin,Rohit@2023# 34.124.244.236 -e \"set ssl:verify-certificate no; mirror --continue --verbose / /root; exit\"'
            }
        }
    }
}
