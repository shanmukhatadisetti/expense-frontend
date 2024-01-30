pipeline {
 agent { label 'workstation' }
  stages {

   stage('Code Quality') {
     when {
                 expression { env.TAG_NAME != env.BRANCH_NAME }

                  }
       steps {
        // sh 'sonar-scanner -Dsonar.host.url=http://54.82.214.251:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=expense-backend -Dsonar.qualitygate.wait=true'
        echo 'CI'
        }
       }
   stage('Release') {
     when {
            expression { env.TAG_NAME == env.BRANCH_NAME }

             }
       steps {
        sh 'env'
        echo 'CI'
        }
       }
   }
 }