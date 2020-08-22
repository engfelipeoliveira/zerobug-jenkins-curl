pipeline {
    agent any

    stages {
        stage("curl") {
            steps {
                script {
                    String response = ""
                    if (isUnix()) {
                        response = sh(script: 'curl -d "token=5db63b48744bb86a21154f28cfd4c446&id_target=129&id=11239" -X POST https://zerobug.co/build.php', returnStdout: true).trim()
                    }else{
                        response = bat(script: 'curl -d "token=5db63b48744bb86a21154f28cfd4c446&id_target=129&id=1456119" -X POST https://zerobug.co/build.php', returnStdout: true).trim()
                    }

                    println("${response}")
                }
            }
        }
    }
}
