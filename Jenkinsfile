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
                        response = bat(script: 'curl -k -u RTOfHaDYLUum7q8jUfDL1598117275:831ef1fc793bade6f7bcfe7d089587b7 --request POST -H "Content-Type:application/json" -d "{\"pit\":\"126\",\"targetid\":\"7wMJ*NG@5sY5PIfKMCTC1598120610\",\"ci\":\"Cicle CI\",\"tipo\":\"6\"}" https://zerobug.co/ScanTarget/', returnStdout: true).trim()
                    }

                    println("${response}")
                }
            }
        }
    }
}
           
           
