#coding:utf-8
"""
综合项目:世行历史数据基本分类及其可视化
作者：王玮璇
日期：2020.6.9

"""

import pygal_maps_world.maps
import math
import pygal
import csv #导入需要用的库


def read_csv_as_nested_dict(filename, keyfield, separator, quote): #读取原csv文件的数据
    
    result={}
    with open(filename,newline="")as csvfile:
        csvreader=csv.DictReader(csvfile,delimiter=separator,quotechar=quote)
        for row in csvreader:
            result[row[keyfield]]=row
    return result
   


pygal_countries = pygal.maps.world.COUNTRIES #在pygal.maps.world读取中国代码
#print(pygal_countries)
