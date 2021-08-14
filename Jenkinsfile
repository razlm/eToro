pipeline {
    agent any

    environment {
        LS = "${sh(script:'helm status etoro | grep STATUS | cut -c 9-', returnStdout: true).trim()}"
    }

    stages {
        stage("Check if 'etoro' helm chars is running") {
            steps {
               script {
                   if (env.LS == 'deployed') {
                       echo "eToro helm chart is running"
                   }
                   else {
                       echo "etoro helm chart is not running"
                   }
            }
        }
    }
        stage("Deploy/Destroy") {
            steps {
               script {
                   if (env.LS == 'deployed') {
                       echo "Destroying helm chart"
                       sh "helm delete etoro"
                   }
                   else {
                       echo "Deploying etoro helm chart"
                       sh "helm install etoro ./etoro"
                   }
            }
        }
    }
}
}
