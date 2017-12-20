node('master') {
  
   stage 'Git Checkout'
     git 'https://github.com/poornimanswamy/spring-petclinic.git'
         echo 'checkout done'

   stage('Maven Build'){
      echo 'Maven Project Compile'
      steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
      steps{
        maven 'clean install' 
      } 
      post {
          success {
              junit 'target/surefire-reports/**/*.xml' 
          }
      }
   }


   stage 'Test Case'
        echo 'Test Case will running'

   stage 'Reporting'
        echo 'Reporting Getting Creating'

   stage 'Job Status Status'
        echo 'Notification Sending'
}
