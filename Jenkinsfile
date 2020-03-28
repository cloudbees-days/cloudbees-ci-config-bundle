library 'cb-days@master'
def masterName = System.properties.'MASTER_NAME'

pipeline {
  agent none
  options {
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    stage('Update Config Bundle') {
      steps {
        configBundleUpdate("${masterName}")
      }
    }
  }
}