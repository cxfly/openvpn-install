http://www.haidongji.com/2015/11/06/%E8%87%AA%E5%BB%BAvpn%E4%B9%8B%E4%B8%89%EF%BC%9A%E6%90%AD%E5%BB%BAopenvpn-service%E5%92%8C%E7%94%9F%E6%88%90%E5%AE%A2%E6%88%B7%E7%AB%AFprofile/

自建vpn之三：搭建openvpn service和生成客户端Profile
给虚机设定了基本的防护措施后，我们来安装openvpn服务器终端并生成profile文件。以下指令都是root级别。我假定你已经通过命令行连到服务器上。请根据需要在命令行前自行添加sudo或变成root。
我原计划给读者提供一步一步的说明，但那样会太繁琐。前两天注意到github上有人已经把这一切打包成一个shell脚本。我今天看了下，觉得写得很好。经过我成功测试后，推荐给你使用。并且这个脚本对Ubuntu，Debian, CentOS, RedHat啥的都管用。
请到 https://github.com/Nyr/openvpn-install 下载openvpn-install.sh脚本文件；
打开命令行，运行：
bash /EnterRightPathHere/openvpn-install.sh
脚本程序会自动探测到你的IP网址，按回车键；
脚本程序让你选择DNS。我不建议第一个选项（Current system resolvers）。2和6均可.
脚本程序让你命名客户端名字。默认是client。我不建议你用默认。建议你根据其所用的设备和数据中心命名，如androidFrankfurt，iphoneFrankfurt，或winPcFrankfurt等等。请用英文字母来命名；
再敲一次回车，程序就开始运行。运行时间差不多三五分钟，请等待，稍安毋躁。
运行结束后，openvpn服务器已经搭建完成并开始运行。接下来你要把它产生的.ovpn文件（profile 文件），比如winPcFrankfurt.ovpn输送到你的Windows/MacBook/Linux/Android/iPhone设备上。强烈建议你用WinSCP（Windows)或scp（Linux/Mac)来输送文件，防止在传送途中被偷窥；
如你需要产生更多的.ovpn文件，只要重新运行
bash /EnterRightPathHere/openvpn-install.sh
并选择第一个选项即可。
祝玩得开心。下一篇，我们来谈谈怎样设立PC、Mac、和Linux客户端来使用vpn。

