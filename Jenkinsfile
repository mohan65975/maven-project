pipeline {
    agent any
    stages{
        stage('Build'){
             steps {
			echo 'Now Archiving...1'
		    	cd "D:/GetHelp Code/maven-project"
		     	echo 'Now Archiving...2'
		     	def sout = new StringBuilder()
			//def args = ['cmd', '/c', 'dir']
			def args = ['cmd', '/c', 'C:\\Program Files\\apache-maven-3.5.0\\bin\\mvn', 'clean' , 'install']
			def proc = new ProcessBuilder( args )
			Process process = proc.start()
			process.consumeProcessOutput( sout )
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
