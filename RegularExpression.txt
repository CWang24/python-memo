By difault, re is always matching in greedy.
To make a non-greedy matching, use the question mark ?.
e.g.
import re
item='abcdddddddddddddd'
pattern = re.compile("a.+")
m=re.findall(pattern,item)
if m:
    res = pattern.search(item).groups()
		print res[0]+'    '+res[1]
		
###################################################
第一个元字符是圆点（.）。在正则表达式中，圆点用于匹配除了换行符外的任何单个字符。
+用于使前面的字符与后面的字符至少匹配一次，
元字符*使得前面的字符可以进行 0次或多次匹配。
元字符？用于使前面的字符进行0次或一次匹配（但是不能超过一次）。
###################################################
\d  匹配任何十进制数；它相当于类 [0-9]。
\D  匹配任何非数字字符；它相当于类 [^0-9]。
\s  匹配任何空白字符；它相当于类  [ \t\n\r\f\v]。
\S  匹配任何非空白字符；它相当于类 [^ \t\n\r\f\v]。
\w  匹配任何字母数字字符；它相当于类 [a-zA-Z0-9_]。
\W  匹配任何非字母数字字符；它相当于类 [^a-zA-Z0-9_]。
###################################################
/\d{5}/  match 5 digits
