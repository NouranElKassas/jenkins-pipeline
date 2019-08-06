pipeline {
      agent any
      stages {
        stage('Upload to AWS.') {
          steps {
              sh 'echo "Hello World"'
              sh '''
                  echo "Multiline shell steps works too"
                  ls -lah
              '''
            }
          withAWS(region:'us-west-2') {
            s3Upload(file:'index.html', bucket:'udacity-jenkins-project-1234', path:'index.html')
            }
        }
        
    }
}
