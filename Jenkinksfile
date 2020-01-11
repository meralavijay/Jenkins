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
          if ($servicestatus -eq "stopped")
           {    
            powershell label: '', script: 'stop-service -name ${env:Servicename}'
           }
           else ($servicestaus -eq "running")
           {
           powershell label: '', script: 'start-service -name ${env:Servicename}'
           }
}
            
         }
       }
     }

}
