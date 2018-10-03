pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
			echo 'Now Archiving...1'
		    	cd "D:/GetHelp Code/maven-project"
		     	"cmd /c mvn clean install".execute()
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
