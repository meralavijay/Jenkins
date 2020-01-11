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
                 if ($servicestatus == "stopped")
           {    
            powershell label: '', script: 'start-service -name ${env:Servicename}'
           }
           else ($servicestaus == "running")
           {
           powershell label: '', script: 'stop-service -name ${env:Servicename}'
           }
           }
}
            
         }
       }
     

}
