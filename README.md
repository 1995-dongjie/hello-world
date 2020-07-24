# hello-world
Hello,everyone!Today is my first day joining Github!
Thanks to Doctor Cao sharing this way to manager my code.
just a study 
# txt和excel文件的打开和读写
 1.txt文件打开和读取
>>> f = open('C:/Users/张灏/Desktop/abc.txt') #注意“\”应该转换为/
>>> str =f.read()
>>> print(str)
>>>hello,word
>>> hello,python
 #2.excel先安装两个包xlrd(读)和xlwt（写）
>>> import xlrd
 >>>import xlwt
 >>>eadbook = xlrd.open_workbook(r'C:\Users\张灏\Desktop\abc.xlsx')
>>> table = readbook.sheet_by_name('English')
>>> nr = table.nrows
>>> nc = table.ncols
>>> va = table.cell(3,1).value
>>> print(va)
546.0
>>> print(nr)
7
>>> print(nc)
3
# 写excel
>>>writebook = xlwt.Workbook()
>>> writebook = xlwt.Workbook(r'C:\Users\张灏\Desktop\abc.xlsx') #workbook中的W要大写
# 抓取网页的方法之正则表达式
>>> import re, urllib.request
			
>>> ur1 = 'http://www.nmc.cn'
			
>>> html = urllib.request.urlopen(ur1).read()
			
>>> html = html.decode('utf-8')
			
>>> links = re.findall('<a target=_"blank"href="(.+?)"title',html)
			
>>> titles = re.findall('<a target="_blank".+? title="(.+?)">',html)
			
>>> tags = re.findall('<a target="_blank".+? title=.+?>(.+?)</a>',html)
			
>>> for link,title,tag in zip(links,titles,tags):
			print(tag,ur1+link,title)

			
>>> print(tag,ur1+link,title)
#正则表达式符号’.’表示匹配任何字符串（除\n之外）；‘+’表示匹配0次或者多次前面出现的正则表达式；‘？’表示匹配0次或者1次前面出现的正则表达式。
# 在网页进行数据爬取
>>>import re
>>> import urllib.request
>>> def getHtml(url):
	page = urllib.request.urlopen(url)
	html = page.read()
	return html

>>> def getImg(html):
	reg = r'src="(.*\jpg)" alt'
	imgre = re.compile(reg)
	imglist = re.findall(imgre,html)
	x = 0
	for imgurl in imglist:
		urllib.urlretrieve(imgurl,'%s.jpg' % x)
		x+=1

		
>>> html = getHtml("http://photo.bitauto.com/?WT.mc_id=360tpdq")
>>> print(html)
 # 奥运五环
>>>import turtle

>>>turtle.width(10)
>>>turtle.color('blue')
>>>turtle.circle(50)

>>>turtle.penup()
>>>turtle.goto(120,0)
>>>turtle.pendown()
>>>turtle.color('black')
>>>turtle.circle(50)

>>>turtle.penup()
>>>turtle.goto(240,0)
>>>turtle.pendown()
>>>turtle.color('red')
>>>turtle.circle(50)

>>>turtle.penup()
>>>turtle.goto(60,-50)
>>>turtle.pendown()
>>>turtle.color('yellow')
>>>turtle.circle(50)

>>>turtle.penup()
>>>turtle.goto(180,-50)
>>>turtle.pendown()
>>>turtle.color('green')
>>>turtle.circle(50)
# 001对象/标识符：一切皆对象（类型、标识、值）
>>> a = 3# a是变量，3是对象
>>> id(3)
1539258656
>>> type(a)
<class 'int'>
>>> print(a)
3
>>> id(a)
1539258656
>>> b = "我爱你"
>>> id(b)
62097408
>>> type(b)
<class 'str'>
>>> print(b)
我爱你
标识符的规则：用于变量、函数、类、模块等的名称：1.区分大小写，如sxt和SXT不同；2.第一个字符必须是字母、下划线，后面接字母、数字、下划线；3.不能用关键字；4.双下划线开头和结尾的表示特殊含义，尽量不用。help(),取消是quit（）。变量的声明：赋值。删除变量和垃圾回收机制。>>> del a .
链式赋值：
