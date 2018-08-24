node('master') {
   checkout scm

stage('Build') {
    // some block
  withMaven(maven: 'M3') {
    // some block
    if (isUnix()){
          sh 'mvn -Dmaven.test.failure.ignore2. clean package'
                  }
    else
        {
        bat 'mvn -Dmaven.test.failure.ignore2. clean package'
         }

    }   
    
    stage ('Results')
    {
    junit '**/target/surefire-reports/TEST-.*.xml'
    archive 'target/*.jar'
    }

              }

  }
