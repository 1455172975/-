#coding:utf-8
"""
第一个小项目：Rock-paper-scissors-lizard-Spock
作者：土木四班李朝锦
日期：2021/11/28
"""

print("欢迎使用RPSLS游戏")
print("----------------")
print("请输入您的选择:")
name=input()
if name in ("石头","史波克","纸","蜥蜴","剪刀") :
        print("你的选择为：",name)
else :
        print("Error: No Correct Name")

import random
number=random.randint(0,4)


# 0 - 石头
# 1 - 史波克
# 2 - 纸
# 3 - 蜥蜴
# 4 - 剪刀

# 以下为完成游戏所需要用到的自定义函数

def name_to_number(name):
    if name=="石头":
        q=0
    elif name=="史波克":
        q=1
    elif name=="纸":
        q=2
    elif name=="蜥蜴":
        q=3
    elif name=="剪刀":
        q=4
    return q
    """
    将游戏对象对应到不同的整数
    """
q=name_to_number(name)
def number_to_name(number):
    if number==0:
        p="石头"
    elif number==1:
        p="史波克"
    elif number==2:
        p="纸"
    elif number==3:
        p="蜥蜴"
    elif number==4:
        p="剪刀"
    return p

def rpsls(name,number):
    if q==0:
            if number==3 or number==4:
                result="你赢了！"
            elif number==0:
                result="您和计算机出的一样"
            else:
                result="机器赢了"
                    
    elif q==1:
            if number==0 or number==4:
                result="你赢了！"
            elif number==1:
                result="您和计算机出的一样"
            else:
                result="机器赢了"
    elif q==2:
            if number==0 or number==1:
                result="你赢了！"
            elif number==2:
                result="您和计算机出的一样"
            else:
                result="机器赢了"
    elif q==3:
            if number==1 or number==2:
                result="你赢了！"
            elif number==3:
                result="您和计算机出的一样"
            else:
                result="机器赢了"
    elif q==4:
            if number==2 or number==3:
                result="你赢了！"
            elif number==4:
                result="您和计算机出的一样"
            else:
                result="机器赢了"
    return result
p=number_to_name(number)
print("计算机的选择为：",p)
choice_name=input()
x=rpsls(name,number)
print(x)



