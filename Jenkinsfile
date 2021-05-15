pipeline
{
  agent any
  
    stages
    {
      stage ("Git Checkout")
      {
        steps
              {
                checkout changelog: true, poll: true, scm: [$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'Bitbucketweb', repoUrl: 'https://github.com/jeetorgn/demorepo'], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'Git User', url: 'https://github.com/jeetorgn/demorepo']]]
               
              }
       }
      stage ("Build")
      {
        steps
        {
          bat 'gradlew.bat clean build'
        }
      }
      
    }
  
}
