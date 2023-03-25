pipeline {
  agent {
    node {
      label 'iac'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        checkout(scm: [$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com//justb1swa/izac2.git']]], poll: true)
      }
    }

    stage('IAC Code Quality Check') {
      steps {
        sh 'cat mytina.sh'
      }
    }

    stage('Environment Build') {
      steps {
        sh 'chmod +x mya.sh'
        sh 'chmod +x mytina.sh'
        sh 'cat mytina.sh'
      }
    }

    stage('terraform init') {
      steps {
        sh 'echo $AWS_ACCESS_KEY_ID'
        sh 'echo $AWS_SECRET_ACCESS_KEY'
        sh 'echo $AWS_SESSION_TOKEN'
        sh './mya.sh'
      }
    }

    stage('terraform in Action') {
      steps {
        sh 'echo $AWS_ACCESS_KEY_ID'
        sh 'echo $AWS_SECRET_ACCESS_KEY'
        sh 'echo $AWS_SESSION_TOKEN'
        sh './mytina.sh'
      }
    }

  }
}
