pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
				echo 'Now Archiving...1'
                		mvn -f "D:/GetHelp Code/maven-project/pom.xml" clean install
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
