# hello-world
Hello,everyone!Today is my first day joining Github!
Thanks to Doctor Cao sharing this way to manager my code.
just a study 
 txt和excel文件的打开和读写
 1.txt文件打开和读取
 f = open('C:/Users/张灏/Desktop/abc.txt') #注意“\”应该转换为/
 str =f.read()
 print(str)
 hello,word
 hello,python
 #2.excel先安装两个包xlrd(读)和xlwt（写）
 import xlrd
 import xlwt
 eadbook = xlrd.open_workbook(r'C:\Users\张灏\Desktop\abc.xlsx')
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
writebook = xlwt.Workbook()
>>> writebook = xlwt.Workbook(r'C:\Users\张灏\Desktop\abc.xlsx') #workbook中的W要大写
