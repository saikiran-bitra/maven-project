pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat '"C:\Program Files (x86)\apache-maven-3.5.2\bin\mvn.cmd" clean package'
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
