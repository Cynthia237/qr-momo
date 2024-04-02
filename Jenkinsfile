pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    environment {
        CI = false
    }    
    stages {
        stage ('sonar analysis') {
            environment {
                scannerHome = tool 'SonarQube=scanner'
            }
            steps {
                withsonarQubeScannerEnv('SonarQube-Scanner
')
            }
        }
    }
}