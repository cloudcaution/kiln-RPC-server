# kiln-RPC-server

声明：
本人为普通码农，此脚本非商用。所有代码均可浏览，无后门，但出任何问题概不负责。
由于本人自己个人用阿里云OSS，流量是付费的请酌情使用下载，如发现滥用，立即停止供应。

使用说明：
使用linux系统 ubuntu20.04， 本人亲测阿里云腾讯云皆可。

1. 打开ubuntu 首先需要打命令：
	sudo -i （进入到root 环境）
2. 然后打  （下载到ubuntu环境）
  注：如果系统显示没有wget 则需打命令：apt update; apt install -y wget 然后打上述命令。
3. chmod +x ./maintain.sh 
4. ./maintain.sh start 
  注：maintan.sh 总共有数个传入参数。分别为：
              start (安装geth和beacon chain /lighthouse 以及启动）
	      check_geth 检查当前geth状态 - 高度 - 区块数据
              check_beacon 检查beacon chain 状态
              python_startup 安装归集脚本python环境
              assembler --addr=0x1234567... 开启归集脚本， --addr=后面是收到归集eth的地址
                                   还有一项需要注意的是 归集的地址集放在一个txt文本， 例子放在 /kiln/ethAddress/ 下面的eth_address_1.txt的里面 

