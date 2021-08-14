pipeline {
    agent any

    environment {
        LS = "${sh(script:'ll flag', returnStdout: true).trim()}"
    }

    stages {
        stage("Env Variables") {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    echo "LS = ${env.LS}"
                }   
            }
        }
    }
}
