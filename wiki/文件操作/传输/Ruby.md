方式一：
```ruby
	 #!/usr/bin/ruby  
	require 'net/http'  
	Net::HTTP.start("www.domain.com") { |http|  
	r = http.get("/file")  
	open("save_location", "wb") { |file|  
	file.write(r.body)  
	}  
	} 
```
 
	执行：ruby test.rb

方式二：
搭建服务器：
ruby -rwebrick -e'WEBrick::HTTPServer.new(:Port => 1337, :DocumentRoot => Dir.pwd).start'  
ruby -run -e httpd . -p 1337