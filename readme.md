1:此项目需要jmeter工具,北京的同事，可以从共享205上将工具下载到ubuntu系统的"主文件夹"目录里。
2:项目名称是construction-api-test
3:construction-api-test项目的结构
	construction-api-test
		|-conf（放一些自动化测试中的配置文件）
                |-src（放一些自动化测试中需要上传的附件文件）
                |-scripts（保存自动化测试中的每一个脚本）
			|-alpha（放alpha环境下的测试脚本）
                    	|-uat（放uat环境下的测试脚本）
                    	|-dev（放dev开发环境下的测试脚本）
		|-report
               		|-alpha（放alpha环境下的测试报告）
                    	|-uat（放uat环境下的测试报告）
                    	|-dev（放dev开发环境下的测试报告）
                |-test.sh(在linux环境下运行的脚本)
                |-readme.md(项目介绍文档)
		|-jmeter.log(运行test.sh脚本后，产生的log日志)

4:这个项目从git上下载后，可以将他放到 /主文件夹/apache-jmeter-2.13/construction-api-test下，
例如我放的目录：/home/chenxuehui/apache-jmeter-2.13/construction-api-test
5:这个项目测的是我本地的样板工程api,所以如果要运行这个test.sh脚本，首先要保证你本地的样板工程能正常启动起来。
6:需要修改/apache-jmeter-2.13/construction-api-test/scripts/dev/modelBackendAPI.jmx脚本里的
 <stringProp name="filename">/home/chenxuehui/apache-jmeter-2.13/construction-api-test/report/dev/${__time(YYMMddHHmm)}_样板工程API_断言结果.csv</stringProp>
<stringProp name="filename">/home/chenxuehui/apache-jmeter-2.13/construction-api-test/report/dev/${__time(YYMMddHHmm)}_样板工程API_察看结果树.csv</stringProp>
这两处，把我的名字修改成你自己的名字。
7:在linux环境下运行test.sh脚本，运行命令是：
~/apache-jmeter-2.13/construction-api-test$ sh test.sh 


