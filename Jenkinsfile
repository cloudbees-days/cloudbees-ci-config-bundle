library 'cb-days@master'
pipeline {
  agent none
  options {
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    when {
      beforeAgent true
      branch 'master'
    }
    stage('Update Config Bundle') {
      steps {
        configBundleUpdate()
      }
    }
  }
}