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
           powershell label: '', script: '''stop-service -name $Servicename
               write-host "The service Status is $Servicename.Staus"''' 
           }
           else
           {
           powershell label: '', script: 'stop-service -name ${env:Servicename}'
           }
           }
}
            
         }
       }
     

}
