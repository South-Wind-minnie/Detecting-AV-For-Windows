﻿Windows杀软检测（检测Windows杀毒软件）
Detecting Anti-virus for Windows
1.0.0
	通过tasklist找出目标系统使用的杀毒软件
	Find out the anti-virus software in the target system through 'tasklist'
	自动识别文件的编码格式
	Automatic recognition of the file's encoding format
	AV字典数据来源(source of data) : https://github.com/gh0stkey/avList/blob/master/avlist.js
	在实际使用中发现这个字典存在一些错误, 所以简单做了一些校对和补充
	In practice, I found some errors in this dictionary, so I made some simple corrections and additions

	Usage：xavd.exe <tasklist.txt>

2.0.0
	没写，构想如下：通过os模块执行tasklist > tasklist.txt，再进行读取操作，之后删除。
	It is not written, the idea is as follows: execute tasklist > tasklist.txt via the os module, then perform a read operation and delete it afterwards.
	使tasklist命令通过代码自动执行，简化操作
	Make tasklist commands automatically executed by code, simplifying operations

3.0.0
	使用psutil模块的proc_iter()，实时读取进程名
	Use the psutil module's proc_iter() to read the process name in real time
	相比之前，减少了体积，提升了速度
	Reduced size and increased speed compared to previous

	Usage：xavd3.exe

本来打算先写3.0.0再写2.0.0，但是3.0.0写出来之后发现2.0.0没必要写，也懒得写。
It was intended to write 3.0.0 before 2.0.0., but after 3.0.0 was written I found that 2.0.0 unnecessary and that I don't want to write with my lazy.
3.0.0已是理想形态（体积控制在个位数MB，速度1秒左右），应该会是最终版本，若有修改也很可能是字典的修改
3.0.0 is the ideal form (single digit MB size, 1 second speed) and should be the final version, with changes, if any, likely to be to the dictionary