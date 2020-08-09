pipeline {
  agent any
  options {
  	withAWS(profile:'aws-static')
  }
  stages {
    stage('Upload to AWS') {
      steps {
        sh '''
          aws s3 cp index.html s3://udacitydevops3.thruniverse.com/index.html
        '''
      }
    }
  }
}
