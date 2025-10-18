pipeline {
  agent any
   environment {
        KUBECONFIG = "/var/lib/jenkins/.kube/config" 
    }
  stages {
      stage('Clone Repo') {
            steps {
                git url: 'https://github.com/ecisneros73/jenkins.git',
                branch: 'main'
            }
        }
      stage('git version') {
            steps {
              sh "git version"
            }
        }  

       stage('maven version'){
            steps {
              sh "mvn -v"
            }
        }  
        stage('Docker version'){
            steps {
              sh "docker -v "
            }
        }    
        stage('Kubernetes version'){
            steps {
              withKubeConfig([credentialsId: 'config']) {
              sh "kubectl version"
              }
            }
        } 
    }
}  
