pipeline {
    agent any

    environment {
        LS = "${sh(script:'ll flag', returnStdout: true).trim()}"
    }

    stages {
        stage("Env Variables") {
            steps {
                echo "LS = ${env.LS}"
            }
        }
    }
}
