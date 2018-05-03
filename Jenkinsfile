pipeline {
  agent any

  stages {
    stage('start') {
      agent any
      steps {
        build (job: 'start', propagate: false)
      }
    }

  stages {
    stage('test_1') {
      agent any
      steps {
        build (job: 'start', propagate: false)
      }
    }

  stages {
    stage('test_2') {
      agent any
      steps {
        build (job: 'start', propagate: false)
      }
    }

  stages {
    stage('test_3') {
      agent any
      steps {
        build (job: 'start', propagate: false)
      }
    }

  stages {
    stage('finish') {
      agent any
      steps {
        build (job: 'start', propagate: false)
      }
    }

  }
}
