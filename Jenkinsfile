pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
			echo 'Now Archiving...1'
		    	dir "D:/GetHelp Code/maven-project"
		     	echo 'Now Archiving...2'
		     	bat "C:/Program Files/apache-maven-3.5.0/bin/mvn.cmd clean install"

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
at
