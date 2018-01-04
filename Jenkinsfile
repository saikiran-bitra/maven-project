pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                mvn clean
                
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
