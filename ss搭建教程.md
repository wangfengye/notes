##　ss搭建教程
1. [github教育邮箱](https://education.github.com/pack/offers#digitalocean)
2. 注册Vultr（性价比高，界面清爽）[打开链接地址](https://www.vultr.com/?ref=7249974)
   使用下面的地址进入注册界面有20美元（有效期一年）的新用户奖励！！
   进入网站后，输入注册邮箱及注册密码，点sign up。
   接下来会收到一封确认邮件，在邮件中点verify your email。到这里账号注册完毕。
3. 充值与配置主机
4. xshell连接主机
5. 部署ss服务
    1. wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
    2. chmod +x shadowsocks.sh
    3. ./shadowsocks.sh 2>&1 | tee shadowsocks.log
        > 中间会提示你输入你的SS SERVER的账号，和端口。不输入就是默认。跑完命令后会出来你的SS客户端的信息。
        请立即copy下来加以保存。
        上面的命令全部回车执行后，如果没有报错，即为执行成功，出现确认提示的时候，输入 y 后，回车即可。
        安装完成后，脚本提示如下：
        Congratulations, shadowsocks install completed!
        Your Server IP:your_server_ip
        Your Server Port:your_server_port
        Your Password:your_password
        Your Local IP:127.0.0.1
        Your Local Port:1080
        Your Encryption Method:aes-v256-cfb 
        保存后关闭
6. 安装SSR加速(centOS 7)
    1. yum --enablerepo=elrepo-kernel -y install kernel-ml kernel-ml-devel
    2. grub2-set-default 0
        > 若版本为centOS6 使用: sed -i 's/^default=.*/default=0/g' /boot/grub/grub.conf
    3. wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh
    4. chmod +x bbr.sh
    5. ./bbr.sh
    6. uname -r ;检查内核版本:含有4.13表示ok
    7. lsmod | grep bbr ;返回值包括 tcp_bbr 模块即说明bbr已启动。




