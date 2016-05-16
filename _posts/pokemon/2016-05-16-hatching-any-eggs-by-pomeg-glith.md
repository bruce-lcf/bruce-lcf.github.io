---
layout: article
title: Hatching Any Eggs by Pomeg Glitch
date: 2016-05-16T20:19:51+08:00
modified:
excerpt:
image:
  feature:
  teaser: lugia.png
  thumb:
avatar: bio-photo.png
ads: false
---

# 利用绿宝石红榴漏洞(Pomeg Berry Glitch)孵化编号386以内的任意PM

## 什么是红榴漏洞？

让有一定HP努力值的PM的当前HP处于1点，再喂给该PM一个红榴果（作用：降低HP努力提升亲密度），会使得该PM的HP变成一个正常游戏中不可能出现的数字。

>举例来说，有一只100级的神奇宝贝有8点HP基础得点，HP是1/100。对它使用红榴后，它的HP基础得点会变为0，这时它的HP就会变成-1/98。但因为游戏在这里使用的数据存储方式是无符号整数存储，HP会变成一个很大的数字，在这例子里就是65535，然后会显示为?35。

![pomeg](http://i1292.photobucket.com/albums/b580/shankenew/glitch_zpsp6ehxhle.png)

****

## 孵化出任意PM的原理

触发红榴漏洞之后，经过一系列操作，会打乱队伍中某个PM的数据组织顺序(Data Substructures)。继而可以让某些数据项成为新的决定PM种类的数据。

第三世代PM的数据组织结构如下表：

![](http://i1292.photobucket.com/albums/b580/shankenew/new_zpsgftuasfy.png)


>The order of the structures is determined by the personality value of the Pokémon modulo 24, as shown below, where G, A, E, and M stand for the substructures growth, attacks, EVs and condition, and miscellaneous, respectively.
	
&nbsp;

>数据子结构的组织顺序取决于PM的PID对24取模的结果。下表中的G，A，E，M分别代表成长(Growth)、攻击(Attack)、努力值及状态(EVs & Conditions)和杂项(Miscellnaneous)。

数据组织顺序如下表：

![order](http://i1292.photobucket.com/albums/b580/shankenew/order_zpsayigkyvu.png)

****

## 一个操作实例：获得一个从蛋中孵出的Deoxys

### 事先的准备

* 一只级别足够高，有一些HP努力值的PM（这里以[#260 Swampert](http://bulbapedia.bulbagarden.net/wiki/Swampert_(Pok%C3%A9mon))为例），用以触发红榴漏洞。下面的叙述中**简称A**。
* 两箱子**完全相同**的某PM，以一定间隔置于1、2号两个箱子（这里以[#064 Kadabra](http://bulbapedia.bulbagarden.net/wiki/Kadabra_(Pok%C3%A9mon))为例，具体间隔可以参考下面的例子），下述**简称B**。这样多数量的同一PM可以使用绿宝石战斗边疆的复制漏洞获得。至于对于这只PM有何具体要求，**在下文中**会详细说明。

### 步骤

 1.将A置于队首，并控制它到1点HP。带上若干只处于濒死状态的PM，最后再带上一只B。	

![step1](http://i1292.photobucket.com/albums/b580/shankenew/step1_zpszf4leukb.png)

 2.喂给A一个红榴果(Pomeg Cherry)，触发漏洞。		 

![step2_a](http://i1292.photobucket.com/albums/b580/shankenew/step2_a_zpsmlbsouox.png) ![step2_b](http://i1292.photobucket.com/albums/b580/shankenew/step2_b_zpsdfwhmtcb.png)	![step2_c](http://i1292.photobucket.com/albums/b580/shankenew/step2_c_zps2az8rwrk.png)	

 3.触发与野生PM的战斗，由A切换到B，然后逃跑。（为了顺利逃跑，建议在PM等级较低的地方进行本步骤）	

![step3_a](http://i1292.photobucket.com/albums/b580/shankenew/step3_a_zpskbgdif30.png)	
![step3_b](http://i1292.photobucket.com/albums/b580/shankenew/step3_b_zps02kglcos.png)	
![step3_c](http://i1292.photobucket.com/albums/b580/shankenew/step3_c_zpsvliyyb1n.png)

4.将B存回电脑的任意一个箱子。	

![step4](http://i1292.photobucket.com/albums/b580/shankenew/step4_zps1vffikmc.png)

5.对A使用任意能够回复HP的道具，下图以高级伤药(Hyper Potion)为例	

![step5](http://i1292.photobucket.com/albums/b580/shankenew/step5_zpshyoyrpmh.png)	![step5_a](http://i1292.photobucket.com/albums/b580/shankenew/step5_a_zpskk2gdtk9.png)

6.再次去野外触发遇敌。

![step6_a](http://i1292.photobucket.com/albums/b580/shankenew/step6_a_zpsibprqd8r.png)	

调出“Pokemon”菜单，查看A的状态	。	

![step6_b](http://i1292.photobucket.com/albums/b580/shankenew/step6_b_zpsqpmz6zvt.png)
![step6_c](http://i1292.photobucket.com/albums/b580/shankenew/step6_c_zpsn1pdfonb.png)	

按下方向键，直到光标正好指到“CANCEL”选项。	

![step6_d](http://i1292.photobucket.com/albums/b580/shankenew/step6_d_zpssialri5v.png)	

**按住**上方向键，直到出现下图所示的情形。然后退出战斗。		

![step6_e](http://i1292.photobucket.com/albums/b580/shankenew/step6_e_zpssw69axlv.png)
![step6_f](http://i1292.photobucket.com/albums/b580/shankenew/step6_f_zps91eu99a0.png)

7.如果足够幸运，你可以在1，2号箱子里的众多坏蛋(bag eggs)中找到一个好蛋(egg)；如果不够幸运，请从步骤1重新来过。	

![step7](http://i1292.photobucket.com/albums/b580/shankenew/step7_zps6h1jmpar.png)

8.将这个蛋孵化，得到目标。

![step8](http://i1292.photobucket.com/albums/b580/shankenew/step8_zpskanqgtqd.png)
![step8_a](http://i1292.photobucket.com/albums/b580/shankenew/step8_a_zpsqhldsjid.png)

****

### 一些重要的补充说明	

最终得到的蛋孵化出什么完全由B决定，所以下面详细解释B和孵化出的东西有何关联。

这里的B，也就是勇吉拉([#064 Kadabra](http://bulbapedia.bulbagarden.net/wiki/Kadabra_(Pok%C3%A9mon)))，我选取了[PID](http://bulbapedia.bulbagarden.net/wiki/Personality_value)为：0x56B0009。经过红榴漏洞，得到的目标的PID会在此基础上加上0x40000000。也就是0x456B0009。0x56B0009对24取模为1，0x456B0009对24取模为17。对应一开始的表格，也就是数据顺序由 **GAME** 变为 **EMAG** 。目标的 **Growth** 对应原来的 **EVs & Conditions**。而 **Growth** 的前两个字节(byte)决定了PM的种类。也就是我们只需要让原来的 **EVs & Conditions** 的前两个字节是我们目标PM的_编号_（要查询编号，请参看[本链接](http://bulbapedia.bulbagarden.net/wiki/List_of_Pok%C3%A9mon_by_index_number_(Generation_III))）。这里 **#386 Deoxys** 的编号16进制下为0x19A，分拆成两个byte就是 0x1 和 0x9A，在十进制下为 1 和 154，也就是我们只需要让勇吉拉([#064 Kadabra](http://bulbapedia.bulbagarden.net/wiki/Kadabra_(Pok%C3%A9mon)))的物攻努力值为1，HP努力值为154，经过红榴漏洞之后，得到的蛋的PM种类对应的就是 #386 Deoxys。

总结：以上改变蛋的物种效果，本质上就是利用游戏漏洞，打乱了原来的数据结构的排列顺序。至于以何种方式打乱，需要知道我们使用的称为“B”的PM的PID是多少，然后查上面提供的表格。一般来说，以努力值(E)代替物种(G)的方法比较普适，可以得到全部的386种PM。

也有一些PID提供了以攻击技能(A)代替物种(G)的置乱方式。具体技能的编码表，我会在最后的参考链接里给出。由于技能数目不足386，这种方式不能获得全部386种PM，但相对上述的以(E)代替(G)的方式也有好处，就是有机会通过这种方式获得理想个体值的PM。上述的那个实例_几乎_无法对获得PM的个体值做任何的控制。

**最后提醒一下**：由于数据被全部打乱，获得的PM的技能会出现非法乱码，为了防止出现死机等不良情况，请把获得的PM放到饲养屋提升足够的等级，用合法技能全部替代后再领出。

吐槽：我获得的这只Deoxys是不听话的，而听话与否由Miscellaneous的最后一个bit决定，然而本例中的置乱方式下，目标的(M)对应的是原来的(A)，最后一个bit和第四个技能的PP数相关，为了使最后一个bit为1，我需要第四个技能的PP数在128以上。而游戏内PP数最大就是64，也就是我无论如何都不可能在游戏内通过这种方式获得一只听话的Deoxys，真是残念。

通过这个漏洞获得的坏蛋可以参与与NPC的战斗，而且可以无限制逃跑，该成果可以应用到绿宝石速通上，然而好像红榴果获得的时机在流程中有些偏后了。

~~利用pomeg glitch向游戏注入汇编代码还在研究中~~

*******************************************

### 参考链接

[视频教程](https://www.youtube.com/watch?v=nOEwPnv2TFM)（Youtube链接）	
	
[Video tutorial for Pomeg Berry Glitch](https://www.youtube.com/watch?v=KME8eusvRAc)（关于红榴漏洞的视频）

Bulbapedia相关页面：

- [Pokémon data substructures in Generation III](http://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_data_substructures_in_Generation_III)
- [List of Pokémon by index number (Generation III)](http://bulbapedia.bulbagarden.net/wiki/List_of_Pok%C3%A9mon_by_index_number_(Generation_III))
- [List of moves](http://bulbapedia.bulbagarden.net/wiki/List_of_moves)（第三世代最后一个技能是 #354 Psycho Boost）
- [Glitzer Popping](http://bulbapedia.bulbagarden.net/wiki/Glitzer_Popping)
