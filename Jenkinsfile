pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat "mvn.cmd clean package"
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
