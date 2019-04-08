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
                    kubeconfigId: 'cid-configfile-minikube',
                    configs: 'k8s/loadbalancer-services.yml',
                    // enableConfigSubstitution: true,
                    // secretNamespace: 'default',
                )
            }
        }
    }
}
