def masterName = System.properties.'MASTER_NAME'

pipeline {
  agent {
    kubernetes {
      yamlFile 'kubectl-pod.yml'
    }
  }
  stages {
    stage('Copy Config Bundle') {
      steps {
        container('kubectl') {
          sh "mkdir ${masterName}"
          sh "cp *.yaml ${masterName}"
          sh "kubectl cp --namespace core ${masterName} cjoc-0:/var/jenkins_home/jcasc-bundles-store/"
        }
      }
    }
  }
}