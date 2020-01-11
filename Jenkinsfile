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
             powershell label: '', script: '''$ServiceStat=get-Service -name ${env:Servicename}
             stop-service -name ${env:Servicename}
             write-host "The service Status is $($ServiceStat.Staus)"'''
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
