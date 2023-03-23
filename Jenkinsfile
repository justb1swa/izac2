pipeline {
    agent {
    node {
      label 'iac'
    }
}
    stages {
        stage('Checkout') {
            steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com//justb1swa/izac2.git']]])            

          }
        }
        
        stage ("terraform init") {
            steps {
                sh ('terraform init') 
            }
        }
        
        stage ("terraform in Action") {
            steps {
                sh ('terraform apply --auto-approve') 
           }
        }
    }
}
