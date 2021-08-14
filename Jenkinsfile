pipeline {
    agent any

    environment {
        LS = "${sh(script:'cat flag', returnStdout: true).trim()}"
    }

    stages {
        stage("Check if pod are up") {
            steps {
                sh 'pwd'
            }
        }
        stage("Env Variables") {
            steps {
                echo "LS = ${env.LS}" 
            }
        }
    }
}
