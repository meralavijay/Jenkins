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
            powershell label: '', script: 'start-service -name ${env:Servicename}'
             write-host "The Status of the ${env:Servicename} is $($servicestatus.Status)" 
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
