pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
				echo 'Now Archiving...1'
                		mvn clean install
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
