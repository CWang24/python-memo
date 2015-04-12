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
[ a b c d e ] 用于匹配a、b、c、d或e中的任何一个字符
[ a - e ] 与上面相同。用于匹配a、b、c、d或e中的任何一个字符
G 用于匹配大写字母G或小写字母g
[ 0 - 9 ] 用于匹配一个数字
[ 0 - 9 ] + 用于顺序匹配一个或多个数字
[ A - Z a - z ] { 5 } 用于匹配任何一组5个字母字符
[ *！＠ # $ % & ( ) ] 用于匹配这些符号中的任何一个
###################################################
/\d{5}/  match 5 digits
