pipeline {
    agent any 
    // environment {
        
    // }
    stages {
        stage('Step 2') { 
            steps {
                echo 'Step 1'
            }
        }
        /* stage('Build') { 
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
        } */
        stage('Publish to Kubernetes') {
            environment {
                VT_SITE_URL = ""
            }
            steps {
                kubernetesDeploy(
                    kubeconfigId: 'kubernetes-cid-minikube',
                    configs: 'k8s/*.yml',
                    // enableConfigSubstitution: true,
                    // secretNamespace: 'default',
                )
            }
        }
    }
}
