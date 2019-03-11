node() {
	
 	stage('checkout'){
 	checkout scm	
	}
 	stage('build env'){
		dir('C:/Jenkins'){
			commit= bat(returnStdout: true, script: 'loopname.py')
			 echo "${commit} "
			 commit.each {
				echo "${it}"

		}
	}
}
  
  
	
	
 		
 
	

