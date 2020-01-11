pipeline
{
  agent any
  stages
     {
     stage ("Servicestatus")
       {
         input 
         { 
           message "Waiting for Approval"
           parameters {string (name:Service,description:This is param from input)}
         steps
          {
            powershell label: '', script: '''$servicestatus = get-service -name ${env:Servicename}
            write-host "The Status of the ${env:Servicename} is $($servicestatus.Status) "
            write-host "The Status from the input  ${env:Service} is $($servicestatus.Status) "'''
          }
         }
       }
     }

}
