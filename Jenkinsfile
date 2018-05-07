// pipeline {
//   agent any

//   stages {
//     stage('start') {
//       agent any
//       steps {
//         build (job: 'start/master', propagate: false)
//       }
//     }

//     stage('finish') {
//       agent any
//       steps {
//         build (job: 'finish/master', propagate: false)
//       }
//     }

//   }
// }

def BuildJob(projectName) {
    try {
       stage(projectName) {
         node {      
           def res = build job:projectName, propagate: false
           result = res.result

           if (result.equals("SUCCESS")) {
           } else {
              error 'FAIL' //sh "exit 1" // this fails the stage
           }
         }
       }
    } catch (e) {
        currentBuild.result = 'UNSTABLE'
        result = "FAIL" // make sure other exceptions are recorded as failure too
    }
}

node {
    BuildJob('start/master')
    BuildJob('finish/master')
}