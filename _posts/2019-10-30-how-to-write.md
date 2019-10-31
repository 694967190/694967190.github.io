---
layout: post
title: 小爬虫
date: 2019/10/30
categories: blog
tags: [Python,编程]
description: 
---

import serial
from time import sleep
import requests
from bs4 import BeautifulSoup
import re

def recv(serial):
    while True:
        data = serial.read(size=17)
        if data == '':
            continue
        else:
            break
        sleep(0.02)
    return data

if __name__ == '__main__':
    serial = serial.Serial('COM5', 9600, timeout=0.5)  #/dev/ttyUSB0
    if serial.isOpen() :
        print("open success")
    else :
        print("open failed")

    while True:
        data =recv(serial)
        if data != b'' :
            st = data.decode('utf-8')
            url = 'http://127.0.0.1:8020/Python/'+ st+'.html?__hbt=1572534552528'
            print(st)
            r = requests.get(url)
            poe = BeautifulSoup(r.text, 'lxml')
            data = poe.select("p")
            for aa in data:
                print(re.sub("<[^>]*>", "", str(aa)))
                print(url)
转载请注明原链接 












