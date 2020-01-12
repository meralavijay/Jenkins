pipeline
{
  agent any
  parameters {string (name:'Path',description:'Input File name')}
  stages
     {
     stage ("ServiceExport")
       {
         
         steps
             {
               powershell label: '', script: 'New-Item -Path C:\\Demo1'
             }
         steps    
               {
               powershell label: '', script: 'Get-Service | Export-Csv -Path C:\\Demo1\Services.csv'
             }
          steps    
               {
               powershell label: '', script: 'New-Item -Path $($Path)'
             }   
           steps    
               {
               powershell label: '', script: 'Remove-Item -Path C:\\Demo1\\Services.csv'
             }    

}
            
         }
       }
     


