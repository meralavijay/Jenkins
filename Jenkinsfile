pipeline
{
  agent any
  parameters {string (name:'Path',description:'Input File name')}
  stages
     {
     stage ("CreateFolder")
       {
         
         steps
             {
               powershell label: '', script: 'New-Item -Path C:\\Demo1'
             }
       }
       
       stage ("Exportcsv")
       {
         steps    
               {
               powershell label: '', script: 'Get-Service | Export-Csv -Path C:\\Demo1\\Services.csv'
             }
     }
        stage ("Customfilename")
       {
           steps    
               {
               powershell label: '', script: 'New-Item -Path $($Path)'
             } 
       }
       stage ("Deletefile")
       {
           steps    
               {
               powershell label: '', script: 'Remove-Item -Path C:\\Demo1\\Services.csv'
             }    

}
            
         }
       }
     


