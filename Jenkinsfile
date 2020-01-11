pipeline
{
  agent any
  stages
     {
     stage ("Servicestatus")
       {
         steps
          {
            powershell label: '', script: '''$servicestatus = get-service -name ${env:Servicename}
            write-host "The Status of the ${env:Servicename} is $($servicestatus.Status) "'''
          }
       }
     }

}
