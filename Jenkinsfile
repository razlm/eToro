pipeline {
    agent any

    environment {
        LS = "${sh(script:'helm status etoro | grep STATUS | cut -c 9-', returnStdout: true).trim()}"
    }

    stages {
        stage("Env Variables") {
            steps {
                    echo "LS = ${env.LS}" 
            }
        }
    }
}
