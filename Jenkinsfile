pipeline {
  agent any
  stages {
    stage('myStage'){
      steps {
        bat 'dir' 
      }
    }
    stage('Build') {
      steps { 
        emailext (
    subject: "Job '${env.JOB_NAME} ${env.BUILD_NUMBER}'",
    body: """<p>Check console output at <a href="${env.BUILD_URL}">${env.JOB_NAME}</a></p>""",
    to: "kola632000@gmail.com",
    from: "kola632000@gmail.com"
    )    
      }
    }
  }
}
