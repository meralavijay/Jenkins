pipeline
{
  agent any
  parameters {string (name:'servicestatus',description:'Provide service Status')}
  stages
     {
     stage ("Servicestatus")
       {
         
         steps
         {
            script
             {
                 if (env.servicestatus == "stopped")
           {    
             powershell label: '', script: '''$Servicestat=get-Service -name ${env:Servicename}
             stop-service -name ${env:Servicename}
             write-host "The service Status is $($Servicestat.Status)"'''
           }
           else
           {
           powershell label: '', script: '''$Servicestat=get-Service -name ${env:Servicename}
             start-service -name ${env:Servicename}
             write-host "The service Status is $($Servicestat.Staus)"'''
           }
           }
}
            
         }
       }
     

}
