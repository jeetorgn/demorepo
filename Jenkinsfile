pipeline
{
  agent any
  
    stages
    {
      stage ("Git Checkout")
      {
        steps
              {
                checkout changelog: true, poll: true, scm: [$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'Bitbucketweb', repoUrl: 'https://github.com/jeetorgn/demorepo.git'], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'Git User', url: 'https://github.com/jeetorgn/demorepo.git']]]
               //git url: 'https://github.com/jfrogdev/project-examples.git'
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
