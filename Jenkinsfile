node('master') {
   checkout scm

stage('Build') {
    // some block
  withMaven(maven: 'M3') {
    // some block
    if (isUnix()){
          sh 'mvn -Dmaven.test.failure.ignore clean package'
                  }
    else
        {
        bat 'mvn -Dmaven.test.failure.ignore clean package'
         }

    }   
    
    stage ('Results')
    {
    junit '**/target/surefire-reports/TEST-*.xml'
    archive 'target/*.jar'
    }

              }

  }
