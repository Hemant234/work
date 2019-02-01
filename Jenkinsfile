node() {
	
 	stage('checkout'){
 	checkout scm	
	}
 	stage('build env'){	
 
 // setx PATH %PATH%;"C:/Users/SESA528099/AppData/Local/Continuum/anaconda3/Scripts"
 def workspace = pwd()
 print "$workspace"
 bat '''cd C:/Python27/Scripts
 set https_proxy=http://165.225.104.32:80
 pip install virtualenv
 cd C:/Program Files (x86)/Jenkins/workspace
virtualenv myproj 
   '''
  }
  	
	stage('install '){ 
	//pip install selenium
	//pip install pymodbus
	//pip install pymodbustcp
	//pip install pandas
	//pip install styleframe
	//pip install wxpython
	//pip install win-inet-pton
	//pip install opencv-python
	//pip install python-appium-client"
	bat '''
        call activate
	IFE_performance.py
	'''
	}	
  
	
	stage('Git'){
	bat '''
	git remote add central https://https://github.com/Hemant234/work.git
	git config --global user.email "tanmai97@gmail.com"
	git config --global user.name "Hemant234"
	git add log1.txt
	git commit -m 'adding a file'
	git push central master
	 '''
	}
	stage('email '){
		 mail body:   'project build successful',
                     from: 'tanmaihemant09@gmail.com',
                     subject: 'project build successful',
                     to: 'hemantbun09@gmail.com'
	}
		

 	}
 	
 		
 
	

