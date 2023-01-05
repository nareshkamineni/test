pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
            ''' 
      }
    }
    stage ('BuilD') {
      steps {
      sh 'mvn clean package'
    }
    
   }
    stage ('SCA') {
      steps {
      sh 'id'
    }
    
   }
      stage ('nikto') {
      steps {
      sh 'nikto -h 3.112.1.112 -p 8080 -o test.html -F html'
    }
    
   }
     
 }
}

