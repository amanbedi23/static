pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps { 
        sh 'echo "Hello World"'
        withAWS(credentials:'aws-static') {
            sh 'echo "Uploading file to s3 bucket"'
            s3Upload(file:'index.html', bucket:'alpha.testbucket', path:'index.html')
        }
      }
    }
  }
}
