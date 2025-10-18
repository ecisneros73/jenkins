pipeline {
  agent any

  stages {
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