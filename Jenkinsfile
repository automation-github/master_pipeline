pipeline {
  agent any

  stages {
    stage('start') {
      agent any
      steps {
        build (job: 'start/master', propagate: false)
      }
    }

    stage('finish') {
      agent any
      steps {
        build (job: 'finish/master', propagate: false)
      }
    }

  }
}
