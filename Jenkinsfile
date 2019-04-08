pipeline {
    agent any 
    environment {
        // BUILD_NUM = "${env.BUILD_NUMBER}"
        // BUILD_TAG = "${env.BUILD_TAG}"

        // DOCKER_REPO_API_URL = "${env.DOCKER_REPO_API_URL ?: "https://index.docker.io/v1/"}"
        // DOCKER_REPO = "${env.DOCKER_REPO}"
        // DOCKER_REPO_CRED = "${env.DOCKER_REPO_CRED}"

        // IMAGE_WEBAPP = "${DOCKER_REPO}:webapp-${BUILD_NUM}"
        // IMAGE_CHAT = "${DOCKER_REPO}:chat-${BUILD_NUM}"
    }
    stages {
        stage('Step 1') { 
            steps {
                echo 'Step 1.1'
            }
        }
        stage('Step 2') { 
            steps {
                sh 'Step 1.2'
            }
        }
        stage('Build') { 
            steps {
                // 
            }
        }
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                // 
            }
        }
    }
}