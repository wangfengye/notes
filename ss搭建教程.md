ss搭建教程
https://education.github.com/pack/offers#digitalocean
1.首先你得有一个paypal账号（如何注册请自行百度）。
       当然，不用paypal直接用visa信用卡也行，但是出于安全性考虑，还是建议大家用paypal。貌似新用户注册有10美元返现，这个我没试过，大家自行搜索。

    2. 注册Vultr（性价比高，界面清爽）
    打开以下链接地址。使用下面的地址进入注册界面有20美元（有效期一年）的新用户奖励！！
  https://www.vultr.com/?ref=7249974
    进入网站后，输入注册邮箱及注册密码，点sign up。



接下来会收到一封确认邮件，在邮件中点verify your email。到这里账号注册完毕。

3.充值与配置
回到Vulrt，在Billing界面按照下图选择好。



虽然可以直接选择绑定信用卡，但是从安全角度考虑，咱们还是老实用paypal吧。这里你要用paypal往Vulrt里充值5美元（具体金额自己定），加上奖励20美元，一共是25美元了（这20美元是一年有效，足够我们花掉它了）。点pay with paypal后是简单的利用paypal的充值过程。

充值完成后，咱们开始配置自己服务器。

点击左边的server选项，然后在页面上方随意取个名字，再按下图依次选择配置：





选好这三个就可以了。点右下角deploy now。会自动跳转到Servers界面。这里耐心等待一两分钟。
当状态显示成下图的running时，咱们的VPS就算全部配置好了。可以点击自己的vps能查看详细信息。



ps：记得抽空去把个人信息填好，如实填写，以避免不必要的麻烦。

3.ss账号的生成
下载PUTTY（或xshell）


解压后运行putty.exe，在主机名称一栏填入vps里分配给你的ip地址，其它不用动，IP地址在哪？如图：



填好后直接点打开按钮：


如果这里有对话框弹出，选择是，然后在全黑的屏幕上输入 root ，回车。等五秒，按提示输入vps的密码，密码在哪？看图：



copy你的密码，粘贴至漆黑屏幕上（粘贴方式为单击鼠标右键，只需要右键单击一次，这里不会显示任何内容，其实是已经输入了），回车。

（以下内容因为我没有将自己已经设置好的账户再次按照步骤操作，无法给出截图，因此这里借鉴了封釉iteke的帖子中的内容，传送门http://bbs.feng.com/forum.php?mod=viewthread&tid=10663132）

等到出现root@vurlt~字样，复制第一条命令：


wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
耐心等待，直到出现root@vurlt~字样，复制第二条命令：
chmod +x shadowsocks.sh
继续等待，
直到出现root@vurlt~字样，复制第三条命令：

./shadowsocks.sh 2>&1 | tee shadowsocks.log

中间会提示你输入你的SS SERVER的账号，和端口。不输入就是默认。跑完命令后会出来你的SS客户端的信息。
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

保存好后关闭putty即可。

4.potatso的下载（苹果）（Android 直接下载shadowsock傻瓜是配置）
利用封釉的付费分享，下载potatso。传送门 http://bbs.feng.com/forum.php?mod=viewthread&tid=10693723
账号失效的请自行在论坛搜寻，也可以出门右拐找surge的使用教程，一样可以达到科学上网，屏蔽各种广告的效果。

5.potatso的设置
进入软件首页，点击右上角加号，添加配置组，名称按你喜好随便取。


点OK。接下来看图操作。





点完成后你会看到自己新建的配置组。



最后，点软件右下角的“更多”——“从二维码导入”扫描下方链接中的二维码。

http://bbs.feng.com/forum.php?mod=viewthread&tid=10592196


显示导入成功后，回到软件首页，选中自己刚刚键的 代|理，然后添加规则组，加入刚刚导入的规则。最终成功如下图：



点连接，开启科学上网与上网无广告之旅。over。

另添加一个教如何优化网速的传送门:http://bbs.feng.com/forum.php?mod=viewthread&tid=10656093