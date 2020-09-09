pipeline {
    agent any
    environment {
        DOCKER_TAG = getDockerVersion()
    }
    stages {
        stage('Build Dokcer Image') {
            sh "docker build -t orientsun6/nodeapp:${DOCKER_TAG}"
        }
    }
}

def getDockerVersion() {
    def tag = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}