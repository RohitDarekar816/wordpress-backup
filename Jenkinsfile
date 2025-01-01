pipeline {
    agent any
    stages {
        stage('Download files from ftp') {
            steps{
                "apt-get update",
                "apt-get install -y lftp curl",
                "apt-get install -y rclone",
                "echo \"Logging into FTP server\"",
                "lftp -u admin,Rohit@2023# 34.124.244.236 -e \"set ssl:verify-certificate no; mirror --continue --verbose / /root; exit\""
            }
        }
    }
}
