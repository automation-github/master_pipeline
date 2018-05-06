def bla = null

pipeline {
  agent any

  stages {
    stage('start') {
      agent any
      steps {
        script {
          bla = "$env.WORKSPACE/build"
          echo bla
        }
        build (job: 'start/master', propagate: false)
      }
    }

    stage('copy xmls') {
      steps {
        sh '''cp -p $bla/*.xml .'''
      }
    }

  }
}
