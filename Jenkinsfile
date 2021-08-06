pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        bat '.\\\\Scripts\\\\UnitTest.bat'
      }
    }

  }
  post {
    always {
      junit '*.xml'
	
	if (currentBuild.currentResult == 'FAILURE')
	{
           step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: "rkrishnanv@laserdepth.com, sendToIndividuals: true])
        } 
    }
  }
}