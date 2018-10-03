pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
			echo 'Now Archiving...1'
		    	cd "D:/GetHelp Code/maven-project"
		     	echo 'Now Archiving...2'
		     	print "cmd /c mvn clean".execute().text

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
