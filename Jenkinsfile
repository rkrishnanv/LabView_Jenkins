pipeline
 {
  agent any
  stages
  {
    stage('Unit Test')
    {
      steps
      {
        bat '.\\\\Scripts\\\\UnitTest.bat'
        junit '*.xml'
      }
    }  
  }
}