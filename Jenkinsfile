pipeline
{
  agent any
  
    stages
    {
   
      stage ("Build")
      {
        steps
        {
          //bat 'gradlew.bat clean build'
          powershell 'gradlew clean build'
        }
      }
      
    }
  
}
