

## erlan 命令行挖矿指南

#### 工具下载说明

> |工具包|系统版本|下载地址|
> |-|-|-|
> |erlan-linux-amd64|linux|[下载地址](https://github.com/erlan/ERLAN-miner/raw/master/ERLAN-linux-amd64/erlan.zip)|
> |erlan-windows-4.0-amd64|winodws|[下载地址](https://github.com/erlan/ERLAN-miner/raw/master/erlan-windows-4.0-amd64.exe/erlan.exe)|
#### linux 系统终端命令行挖矿指南

  1. 准备工作
	
  - linux 下载 erlan 到本地目录
````
  # 打开终端sudo -s 进入root根目录
  
  # 在终端输入复制hap 到bin目录：
    mv erlan /usr/local/bin  

  # 授给erlan授权：
    chmod +x /usr/local/bin/hap
  # 下载start.sh 并复制到/home/目录,修改start.sh中的矿工账户为你的个人账户
    打开终端 sudo -s 回车授权
    chmod +x start.sh
    ./starth.sh 启动后台挖矿，关闭终端不受影响。    
````
#### Window 系统CMD命令行挖矿指南
 
 启动挖矿
 
````
  # 下载
    下载对应的操作系统版本，并改名为erlan.exe，新建d:/erlan目录，复制erlan到d:/erlan目录

  # 启动控制台
    win+R 启动cmd 窗口

  # 进入D盘下的hap目录
    D:        //在CMD输入D：回车进入D盘
    cd erlan  //进入erlan目录

  # 进入erlan console控制台
    erlan console 

  # 生成挖矿账户,注意保存账户地址，密码和对应的keystore
    personal.newAccount("你的密码")

  # 启动挖矿
    miner.start()  
```` 
#### Mac 系统挖矿指南（同linux)
#### 其他系统，理论上支持，但不建议
#### 常用命令：
     # erlan console与erlan attach都是交互式控制台，只能选用一个,于控制台下执行下述命令：
     # 生成账户：personal.newAccount("1345666")  替换“”中的密码为自己的
     # 启动挖矿：miner.start()  //适用于控制台下启动挖矿，最好关闭控制台，用erlan --mine启动后台挖矿。
     # 查挖矿账户余额：eth.getBalance(eth.coinbase)
     # 查询特定账户余额：eth.getBalance("0x60c8abe58c9dbc52a4ee9f......“) 替换“”中的账户为要查询的， 
     # 节点连接查询：admin.peers 
     # 命令行转账：
     ##personal.unlockAccout("账户“）
     ##eth.sendTransaction({from: '0x544.......', to: '0x02df.......', value: 100000000}) 
#### 在线钱包配套挖矿使用(适用于挖矿中的电脑）
     #wallet.erlan.ink //打开这个网站
     #pkill erlan  //关闭现有挖矿进程：
     #erlan --rpc --ws --wsorigins "wallet.erlan.ink" --mine //终端执行这条命令（替代erlan console)、块高，同步完成后可转账操作\自动挖矿。
     #personal.unlockAccount("你的账户")  //在线钱包连接到节点并同步完成后，可使用这个命令解锁你的账户，然后利用在线钱包转账。
     
     
