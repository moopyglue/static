pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-2',profile:'aws-static') { 
          s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacitydevops3.thruniverse.com', path:'/index.html')
        }
      }
    }
  }
}
