pipeline {
  agent {
      label ('NODEJS')
  }

  stages {
    
    stage('Download Dependencies') {
      steps {
        sh '''
          mvn clean package
        '''
      }
    }

    stage('Prepare Artifacts') {
      steps {
        sh '''
          cp target/*.jar users.jar 
          zip ../users.zip users.jar
        '''
      }
    }  

    stage('Upload Artifact') {
      steps {
        sh '''
         curl -v -u admin:admin123 --upload-file /home/ubuntu/workspace/TODO_CI-Pipelines/users.zip http://172.31.52.12:8081/repository/users/users.zip
        '''
      }
    }
  }

}