pipeline {
  agent {
      label ('NODEJS')
  }

  stages {
    
    stage('Compile Code') {
      steps {
        sh '''
          mvn compile
        '''
      }
    }

    stage('Make Package') {
      steps {
        sh '''
          mvn package
        '''
      }
    }

    stage('Prepare Artifacts') {
      steps {
        sh '''
          cp target/*.jar users.jar 
          zip -r users.zip users.jar
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