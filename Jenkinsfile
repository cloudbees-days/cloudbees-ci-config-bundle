@Library('cb-days@master') _
pipeline {
  agent none
  options {
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
    timeout(time: 30, unit: 'MINUTES')
  }
  stages {
    stage('Update Config Bundle') {
      when {
        beforeAgent true
        branch 'master'
      }
      steps {
        configBundleUpdate()
      }
    }
  }
}
