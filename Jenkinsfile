node ('master') {

  stage ('SCM') {
    checkout([$class: 'GitSCM', 
        branches: [[name: '*/master']], 
        extensions: [], 
        userRemoteConfigs: [[url: 'https://github.com/ganeshhp/helloworldweb.git']]])
   }
  
  stage ('maven-build') {
    sh 'mvn clean package'
   }
   
  
    mail bcc: '', 
    body: 'Job Status', cc: '', 
    from: '', replyTo: '', 
    subject: 'Failure ${env.JOB_NAME}', 
    to: 'plusforum.in@gmail.com'
 
 }
