pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
				echo 'Now Archiving...1'
		    cd "D:/GetHelp Code/maven-project"
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
