方式一：
	#!/usr/bin/php 
	<?php $data = @file("http://192.168.1.192/Client.exe");
	$lf = "1.exe";         
	$fh = fopen($lf, 'w');         
	fwrite($fh, $data[0]);         
	fclose($fh); 
	?>

方式二：
	<?php  
	$url  = '[http://www.example.com/file](http://www.example.com/file)';  
	$path = '/path/to/file';  
	$ch = curl_init($url);  
	curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);  
	$data = curl_exec($ch);  
	curl_close($ch);  
	file_put_contents($path, $data);  
	?>  	 
	
  执行：php test.php

方式三：
PHP 5.4+
搭建服务器
	php -S 0.0.0.0:1337