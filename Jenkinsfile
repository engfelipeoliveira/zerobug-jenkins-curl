pipeline {
  agent any
    stages {
        stage("curl") {
            steps {
                script {
                    String response = ""
                    if (isUnix()) {
                        response = sh(script: 'curl -k -u $ZEROBUGUID:$ZEROBUGTOKEN --request POST -H "Content-Type:application/json" -d "{"pit":"130","targetid":"O4naF1!C*IdpKq4DWk9B1598286997","ci":"Jenkins","tipo":"11"}" https://zerobug.co/ScanTarget/', returnStdout: true).trim()
                      }else{
                        response = bat(script: 'Invoke-RestMethod -uri "https://zerobug.co/ScanTarget/" -ContentType "application/json; charset=UTF-8"  -Method POST -Headers @{ Authorization = "Basic $([System.Convert]::ToBase64String([System.Text.Encoding]::ASCII.GetBytes($env:ZEROBUGUID +":"+$env:ZEROBUGTOKEN)))"} -Body $(@{pit="130";targetid="O4naF1!C*IdpKq4DWk9B1598286997";ci="Jenkins";tipo="11"}| ConvertTo-Json)', returnStdout: true).trim()
                    }

                    println("${response}")
                }
            }
        }
    }
}
           
           
