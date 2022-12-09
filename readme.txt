

把这个setup.sh放机器上去。和aleo-prover-cuda在同目录下

通过vim 编辑一个config.cfg的文件
ACCOUNT_NAME=accountname
POOL="xxx.xxx.xxx.xxx:xxxx"

配置好代理软件的地址，然后首次执行就是这个命令来首次安装,一定得是sudo权限，
运行setup.sh本身自带了start功能,程序会自动启动
sudo ./setup.sh

检查程序是否启动成功
ps aux |grep aleo
看看是否有进程列表
等待3分钟后是否可以在prover.log里面看到类似的日志
2022-12-09 00:19:41.041  INFO 2.1.2 474322 perf: 870059 (1m: 1319.02 P/s, 5m: 1317.87 P/s, 30m: --- P/s, 60m: --- P/s)
2022-12-09 00:20:41.042  INFO 2.1.2 474322 perf: 949274 (1m: 1320.25 P/s, 5m: 1318.25 P/s, 30m: --- P/s, 60m: --- P/s)
2022-12-09 00:21:41.043  INFO 2.1.2 474322 perf: 1028496 (1m: 1320.37 P/s, 5m: 1319.03 P/s, 30m: --- P/s, 60m: --- P/s)
2022-12-09 00:22:41.044  INFO 2.1.2 474322 perf: 1107681 (1m: 1319.75 P/s, 5m: 1319.43 P/s, 30m: --- P/s, 60m: --- P/s)


后续执行就是那个执行即可
./start_aleo.sh

暂停
./stop_aleo.sh

查看日志
tail -f prover.log
