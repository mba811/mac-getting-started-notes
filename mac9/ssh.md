# Mac下的穩定SSH軟體-Secret Socks

在介紹socket socks軟體之前先介紹一下ssh，什麼是ssh?

**SSH**是**Secure Shell**的縮寫，由[IETF](http://zh.wikipedia.org/wiki/IETF)的网络工作小组所制定，是一種比普通ftp,telnet,pop網絡傳輸服務都要更加為安全的傳輸協議。普通傳輸協議都可以被別人竊聽到，但是使用ssh來傳輸信息，可以有效地對信息進行加密和壓縮，防止DNS欺騙和IP欺騙，同時對信息數據的壓縮也能大大地減少傳輸時間。SSH最初使用與unix系統，之後又迅速普及到其它操作系統(更詳細的解釋可以參考[wiki](http://zh.wikipedia.org/wiki/SSH))

而在mac系統下實現ssh連接可以使用在終端上使用命令的方法，例如是：
    
    ssh -D portnumber username@hostname

不過每次都要輸入密碼，還有斷線了要再手動輸入命令連接，這樣比較麻煩，對於不想使用命令的人來說，用直觀人性化的圖形介面軟體則是更加為之方便的了。

Mac下的ssh圖形介面的軟體有很多，例如我曾經使用過的**issh**，連接是可以連接到，但是我發現這款軟件不穩定（並非是我的ssh帳號不穩定），經常都會自動掉線，所以也就不再使用這款軟件了。到後來我發現了**Secret Socks**這款軟件，經過我長久的使用情況，發現這款軟件還是比較穩定的，直到現在還沒有出現過掉線的情況，所以在這裡就推薦給大家使用。

[![](http://m3.img.srcdd.com/farm5/d/2012/1207/09/27CE3510DB158A5E0A71C112B5D03F7D_B500_900_220_220.JPEG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/secretsockss.jpg)

**項目主頁**：[點擊進入](http://nihilex.com/secret-socks)

**官方下載地址**：[點擊下載](http://socks.nihilex.com/SecretSocks-1.0.2.dmg)

為了防止官網被Q掉，我放在**uudisc上的下載地址**：[點擊下載](http://www.uudisc.com/user/kanonsola/file/4208624)

### 下面說說使用方法：

1：在Mac系統下下載回來後雙擊打開它：

[![](http://m3.img.srcdd.com/farm5/d/2012/1207/09/D328D7BDCE5F35F7EB77A8D138ED52FC_B500_900_182_118.PNG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/Finder3.png)  
2：出現運行警告框，點擊“**Open**”打開：

[![](http://m2.img.srcdd.com/farm4/d/2012/1207/09/DF94FEBACD825C49B1F35AB5E0301728_B500_900_439_178.JPEG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/31.jpg)  
3：彈出窗口，把左邊的**Secret Socks**程序拖到右邊的**Applications**文件夾裏：

[![](http://m2.img.srcdd.com/farm5/d/2012/1207/09/9356F596D9CD6289C2A13F32D129B51E_B500_900_433_415.JPEG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/4.jpg)

4：然後打開“**Applications**”應用程序文件夾，找到“**Secret Socks**”把它打開：

[![](http://m2.img.srcdd.com/farm4/d/2012/1207/09/37EBB782E80B13E84819949067569B61_B500_900_500_378.JPEG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/51.jpg)

5：軟件介面，非常簡潔，介紹一下軟件介面：

**SSH hostname**:SSH主機地址

**Port number**:端口號碼，這個我們一般填22

**Obfuscation key**:這個如果你的SSH服務器擁有Obfuscation-openssh key（不是很明白），那麼則把你的服務器的keyword(關鍵字?)填上去，沒有的話則把它留空白，這個不同於ssh密碼，不過一般都不用填。

**Username**：SSH帳號名

**Password**：SSH密碼

**SOCKS port**:Socks端口，這個不用改也可以,建议改为7070

填好了相關信息後點擊上面的“**Connect**”按鈕連接ssh：

 

[![](http://m1.img.srcdd.com/farm4/d/2012/1207/09/19C5BDFBA89FA685913D6BD4974FCCEA_B500_900_500_419.JPEG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/6.jpg)

6：假如連接成功了右邊就會在右邊顯示一個大大的綠色的勾，點擊回“**Disconnect?**”會切斷ssh連接：

[![](http://m2.img.srcdd.com/farm4/d/2012/1207/09/E121FCF88B971DCF4B00CE1240ADD801_B500_900_500_424.PNG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/SecretSocks3.png)

7：切換到“**Sautus**”可以查看連接狀態：

[![](http://m2.img.srcdd.com/farm5/d/2012/1207/09/460652C50B4631091E4F8DC761981B11_B500_900_500_423.PNG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/SecretSocks2.png)

8：切換到“**Help**”可以查看幫助信息。

[![](http://m2.img.srcdd.com/farm4/d/2012/1207/09/BF4A3662B4EF89167BDC48C4E0C6E3EA_B500_900_500_433.PNG)](http://www.pairsdoll.com/wp-content/uploads/2011/08/SecretSocks.png)  
secret socks軟體所採用的命令如下：
    
    ssh -ND 9999 -p portnumber username@hostname

加上obfuscated-openssh使用時,則命令如下:
    
    ssh -ND 9999 -p portnumber -zZ key username@hostname

 

這樣SSH就能成功連接到了，至於ssh能做什麼，我這裡就不再說下去了，下面提供一些免费SSH帐号:

1:由[老T](https://fuck.aenes.com/)赞助的免费SSH帐号，免費帳號每30分钟自动改变密码，既是每30分鐘斷開一次连接：（测试可用）

免费SSH服务器1:74.117.62.55        账户:freessh      密码:[](https://fuck.aenes.com/s1.php)

免费SSH服务器2:205.185.121.173  账户:freessh      密码:[](https://fuck.aenes.com/s2.php)

免费SSH服务器3:74.82.188.170     账户:freessh      密码:[](https://fuck.aenes.com/s3.php)

——————————我是华丽的分割线——————————–

2:由[onlybird](http://blog.onlybird.com/%E5%85%8D%E8%B4%B9ssh%E4%BB%A3%E7%90%86)提供的免费SSH帐号,端口为9999,一号服务器的密码每4小时更新一次，其余服务器的密码每24小时更新一次,请直接到这个网站去获取:[点击进入](http://blog.onlybird.com/%E5%85%8D%E8%B4%B9ssh%E4%BB%A3%E7%90%86).（测试不可用）

——————————我是华丽的分割线——————————–

3:由[SSH heyxin](http://ssh.heyxin.com/)网站提供的免费SSH账号：（测试可用，连接速度快）

服务器 [ssh.heyxin.com](http://ssh.heyxin.com/) 端口 22        账户:best           密码 best

服务器freessh.eu            端口 22       账户:best            密码 best

密码可能随时会变，发现密码不能用了请到[网站](http://ssh.heyxin.com/)查看最新密码。

——————————我是华丽的分割线——————————–

4:由[bestssh.net](http://bestssh.net/)提供的免费SSH账号：（测试可用）

服务器：ssh.heyxin.com 端口：22  账户:freessh      密码:c8OA2otj%

密码可能随时会变，发现密码不能用了请到[网站](http://bestssh.net/free-ssh-account/)查看最新密码。

——————————我是华丽的分割线——————————–

5：由[SSH4gfw](http://www.ssh4gfw.com/)网站提供的免费SSH账号，免费使用一年：（测试可用）

请到[网站](http://www.ssh4gfw.com/)里注册新用户，然后到产品页面直接获取免费账号，过程这里不细说。

嫌麻烦可用使用我在上面网站注册得来的免费账号：

服务器:temp1.ssh4gfw.com 端口:22 账户:tm-0004096 密码：0292424  到期时间:2012-09-21

——————————我是华丽的分割线——————————–

6：网上搜集得来的一个可以用一年的免费SSH账户：（测试可用）

服务器:ssh2.nbvp.info         端口:22  账户:fdblog             密码：pass           到期时间:2012-09-22
