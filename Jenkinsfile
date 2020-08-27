pipeline {
    agent any

    stages {
        stage("curl") {
            steps {
                script {
                    String response = ""
                    if (isUnix()) {
                        response = sh(script: 'curl -k -u ${ZEROBUGUID}:${ZEROBUGTOKEN} --request POST -H "Content-Type:application/json" -d "{"pit\\":\\"131\\",\\"targetid\\":\\"kXtS1wWamk9Uc5QP2i0N1598530195\\",\\"ci\\":\\"Jenkins\\",\\"tipo\\":\\"11\\"}" https://zerobug.co/ScanTarget/', returnStdout: true).trim()
                    }else{
                        response = bat(script: 'curl -k -u ${ZEROBUGUID}:${ZEROBUGTOKEN} --request POST -H "Content-Type:application/json" -d "{\\"pit\\":\\"131\\",\\"targetid\\":\\"kXtS1wWamk9Uc5QP2i0N1598530195\\",\\"ci\\":\\"Jenkins\\",\\"tipo\\":\\"11\\"}" https://zerobug.co/ScanTarget/', returnStdout: true).trim()
                    }

                    println("${response}")
                }
            }
        }
    }
}
