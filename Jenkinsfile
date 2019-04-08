pipeline {
    agent any 
    environment {
        NGINX_VERSION = "nginx:1.7.9"
    }
    stages {
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
                    // kubeconfigId: 'cid-configfile-minikube',
                    credentialsType: 'KubeConfig',
                    kubeConfig: [path: '/home/sg/.kube/config'],
                    configs: 'k8s/*.yml',
                    // enableConfigSubstitution: true,
                    // secretNamespace: 'default',
                )
            }
        }
    }
}
