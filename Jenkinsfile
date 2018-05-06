def bla = null

pipeline {
  agent any

  stages {
    stage('start') {
      agent any
      steps {
        script {
          bla = "$env.WORKSPACE/build"
          echo $bla
        }
        build (job: 'start/master', propagate: false)
      }
    }

    stage('test_1') {
      agent any
      steps {
        build (job: 'test_1/master', propagate: false)
      }
    }

    stage('test_2') {
      agent any
      steps {
        build (job: 'test_2/master', propagate: false)
      }
    }

    stage('test_3') {
      agent any
      steps {
        build (job: 'test_3/master', propagate: false)
      }
    }

    stage('finish') {
      agent any
      steps {
        build (job: 'finish/master', propagate: false)
      }
    }

    stage('copy xmls') {
      steps {
        sh '''cp -p ${workspace_179_12}/*.xml .'''
      }
    }

  }
}
