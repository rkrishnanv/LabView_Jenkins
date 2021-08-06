pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        bat '.\\\\Scripts\\\\UnitTest.bat'
      }
    }

    stage('Results') {
      steps {
        junit '*.xml'
      }
    }

  }
  post {
    always {
      junit '*.xml'
    }

  }
}