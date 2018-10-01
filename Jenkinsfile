pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
				echo 'Now Archiving...1'
                cmd.exe /C '""C:\Program Files\apache-maven-3.5.0\bin\mvn.cmd" clean package'
				echo 'Now Archiving...2'
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