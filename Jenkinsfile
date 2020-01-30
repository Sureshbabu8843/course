pipeline {
  agent any
  stages{
    stage('Build'){
      steps {
              sh 'mvn clean package'
      }
        post {
          success { 
              echo 'Now Archiving...'
              archiveArtifacts artifacts: 'course.war'
          }
        }
     }
    
    stage ('Deployments'){
      parallel{
        stage ('Deploy to Staging'){
          steps {
                sh "cp course.war /usr/local/apache-tomcat8/webapps"
          }
        }
      }
      post {
        success {
          mail to: 'gsureshbabu4321@gmail.com', subject: 'job is success', body: 'this is test'
        }
      }
    }
  }
}
