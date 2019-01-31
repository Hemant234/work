node() {
	
 	stage('checkout'){
 	checkout scm	
 	stage('build env'){	
 
 // setx PATH %PATH%;"C:/Users/SESA528099/AppData/Local/Continuum/anaconda3/Scripts"
 def workspace = pwd()
 print "$workspace"
 bat '''cd C:/Python27/Scripts
 set https_proxy=http://165.225.104.32:80
 pip install virtualenv
 cd C:/Program Files (x86)/Jenkins/workspace
virtualenv myproj --python= C:/Users/SESA528099/PycharmProjects/hope2/venv/Scripts/python.exe
   '''
  }
  

	}
	
	stage('install '){ 
	bat '''
	cd Scripts
  activate
  cd ..
	pip install selenium
	pip install pymodbus
	pip install pymodbustcp
	pip install pandas
	pip install styleframe
	pip install wxpython
	pip install win-inet-pton
	pip install opencv-python
	//pip install python-appium-client"
	'''
	}
	stage('build '){
	try {
  	bat '''
  	 cd Scripts
  	activate
  	cd ..
  	IFE_performance.py
  	'''
  }
  catch(err){
  	print " Script is not running"
  }	
  
	}
	stage('Git'){
	bat '''
	 git config --global http.proxy http://165.225.104.32:80"
	 git add *"
	 git commit -m * "	
	 git push origin master
	 '''
	}
	stage('email '){
		 mail body:   'project build successful',
                     from: 'tanmaihemant09@gmail.com',
                     subject: 'project build successful',
                     to: 'hemantbun09@gmail.com'
	}
		

 	}
 	
 		
 
	

