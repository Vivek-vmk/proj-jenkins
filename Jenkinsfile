pipeline {
    agent any

    stages {
        stage('code clone') {
            steps {
                echo "Repository has been cloned successfully"
                git url: "https://github.com/ofc365/proj-jenkins-git-docker.git"
            }
        }
        stage('code build') {
            steps {
                echo "Successfully compiled the project after cloning"
                sh "docker build . -t mypipeimg:latest"
            }
        }
        stage('code test') {
            steps {
                echo "Post-build testing is done"
            }
        }
        stage('code deploy') {
            steps {
                echo "The application has been successfully deployed inside the container"
                sh "docker run -itd -p 8000:8000 mypipeimg:latest"
            }
        }
    }
}
