pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                call mvn clean
                
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
