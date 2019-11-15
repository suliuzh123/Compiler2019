# 编译原理实验

最新实验内容和通知请参考: https://github.com/suliuzh123/Compiler2019

> 2019-11-15 *更新Lab3加分项要求*

> 2019-11-10 *Lab3更新提交文件结构,统一命名*

> 2019-11-04 *Lab2提交周五23:59:59截止, Lab3公布*

> 2019-10-31 *Lab2提交日期延至11.8 23:59:59(下周五), Lab3下周一公布"*

> 2019-10-14 *Lab1提交今晚19:59:59截止,  Lab2公布*

> 2019-09-23 *Lab1和分组名单已公布*

> 2019-09-20 *公布分组要求*


----

## 基本内容

实验教材为: *《编译原理实践与指导教程》，许畅 陈嘉 朱晓瑞编著*

助教邮箱
- suliuzh123@163.com
- wangz@smail.nju.edu.cn

### 总体要求:
1. 每次实验在截止日期之前提交到助教邮箱: suliuzh123@163.com

2. 每次实验提交内容只包含一个压缩包文件: 组长学号_姓名_Lab*X*_v*Y*_group*Z*.zip, 邮件标题为 "Compiler2019-Lab*X*", 其中*X*表示第几次实验, *Y*表示第几次版本, *Z*表示分组号码, 使用具体信息替换 *XYZ*(如"17122xxxx_张三_Lab1_v1_group5.zip")

3. 压缩包内容示例 Lab.zip 所示, 包含源程序, 可执行文件, 实验报告(2-3页)等, 提交时注意文件名命名

4. 使用给定 Makefile 进行编译, 自己另外构造的Makefile或者脚本无效

5. 提交内容按上述指定要求进行提交, 违反者会进行倒扣分


----



## 实验3 中间代码生成

本次实验任务是在词法分析、语法分析和语义分析程序的基础上，将C--源代码翻译为中间代码。
实验要求将中间代码输出成线性结构，从而可以使用虚拟机小程序（附录B）来测试中间代码的运行结果。


指选内容: 要求3.1, 3.2, 2选1, 每组只需完成一个选做要求, 多做不得分
- 选做3.1: 奇数组号 (e.g. 组号为1,3,5,...,选做3.1)
- 选做3.2: 偶数组号 (e.g. 组号为2,4,6,...,选做3.2)


评分标准：

1. 基本: 按照提交要求提交指定内容(源程序,可执行文件,实验报告), 程序可以通过 Makefile 编译和运行;
2. 必做内容: 对所有的组, 测试用例相同, 输出要求相同;
3. 指选内容: 对不同的组, 测试用例相同, 输出要求不同;
4. 可选内容: 会设置测试用例用于加分(2个测试用例,只包含必做要求,会有大量的优化空间,所有的组都会进行测试)
	- 对于每个测试用例, 能够正确翻译,保证结果正确会有5的加分
	- 对于每个测试用例, 进行中间代码优化测试效率, 在正确翻译的前提下能够在运行效率排名Top5(10%), Top15(30%), Top25(50%)的组进行20,15,10加分
	- 实验三加分最多为 (5 + 20) * 2 = 50 分, 满分最多为 165 (150\*1.1)
> 对于额外加分的测试用例, 程序中的可优化点有多个如公共表达式,临时变量等, 但是前提是需要保证中间代码的正确性，要能准确输出最后的结果,才会进行优化测试.


虚拟机小程序执行文件：irsim.zip (解压后按照附录要求安装依赖,`python irsim.pyc`执行）

<!--
实验注意事项和问题
详见 [Lab3要求.md](Lab3要求.md)

> 持续更新中, 请关注
-->

**提交文件结构**
```
/组长学号_姓名_LabX_vY_groupZ
	/Code			# 所有的代码均在此目录下
		Makefile	# 提交时不要对此文件进行修改
		lexical.l
		syntax.y
		main.c
		...
	/Test			# 提交时不要对此文件夹进行修改
		test1.cmm
		test2.cmm
	report.pdf		# 提交时请替换此文件,注明姓名,学号和联系邮箱,文件命名为report.pdf,2-3页
	parser			# 提交时请用编译后的文件替换此文件
	README
```
请将上述文件夹压缩成`组长学号_姓名_LabX_vY_groupZ.zip`提交

提交时保持**正确的目录结构**和**文件夹命名**方式, 对上述不可修改文件部分,测试时会进行统一的替换


**截止日期:**

- 2019年11月29日 23:59:59 周五晚之前提交
- 邮箱： suliuzh123@163.com
- 邮件标题为：Compiler2019-Lab3-groupZ
- 邮件压缩包内容为：组长学号_姓名_LabX_vY_groupZ.zip


----

## 实验2 语义分析

详见 [Lab2要求.md](Lab2要求.md)


----

## 实验1 词法分析与语法分析

详见 [Lab1要求.md](Lab1要求.md)



