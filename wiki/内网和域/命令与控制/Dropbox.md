	>git clone https://github.com/Arno0x/DBC2 dbc2
	>cd dbc2
	>pip install -r requirements.txt
	>chmod +x dropboxC2.py
	https://www.dropbox.com/developers/apps/create
	创建好后要生成个accesstoken，填入config.py中
![image](img/269.png)

	执行
![image](img/270.png)

	这里需设置一个与受控机交互的加密密码
	发布agent
	>publishStage dbc2_agent.exe
	使用命令listPublishedStage可以看到已发布的agent
![image](img/271.png)

	生成payload
	>genStager [tab]查看可生成的格式
![image](img/272.png)

	>genStager oneliner default生成powershell格式payload
![image](img/273.png)

	>genStager batch default生成bat格式
![image](img/274.png)

	Msbuild，其余不做演示
![image](img/275.png)

	这里使用powershell格式的，在受控机运行
![image](img/276.png)

	攻击机可以看到上线
![image](img/277.png)

	>list命令可以看到已控机器
![image](img/278.png)

	使用use命令与受控机器交互
![image](img/279.png)

	输入?获得后续命令
![image](img/280.png)