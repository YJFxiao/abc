# abc
abc
url='https://s.taobao.com/search?q=%E8%A3%99%E5%AD%90&imgfile=&commend=all&ssid=s5-e&search_type=item&sourceId=tb.index&spm=a21bo.2017.201856-taobao-item.1&ie=utf8&initiative_id=tbindexz_20170306&ajax=true'
import urllib.request as r
data=r.urlopen(url).read().decode('utf-8','ignore')

import json
data=json.loads(data)

def info(i):
    print(data['mods']['itemlist']['data']['auctions'][i]['title'])
    print(data['mods']['itemlist']['data']['auctions'][i]['view_price'])
    print(data['mods']['itemlist']['data']['auctions'][i]['item_loc'])
    print(data['mods']['itemlist']['data']['auctions'][i]['view_sales'])
def infoprint(a):
    info(a)
    info(a+1)
    info(a+2)
    info(a+3)
    print('-'*20)
infoprint(0)
infoprint(4)
infoprint(8)
infoprint(12)
infoprint(16)
infoprint(20)
infoprint(24)
infoprint(28)
infoprint(32)

def message():
    for i in range(0,36):
        print('第'+str(i+1)+'件商品的信息为：'+data['mods']['itemlist']['data']['auctions'][i]['title'])
        
message()

da=[]
def  getprice():
    for a in range(0,36):
        print(data['mods']['itemlistdata']['']['auctions'][a]['view_price'])
        da.append(float(str(data['mods']['itemlist']['data']['auctions'][a]['view_price'])))
        
getprice()

db=sorted(da)

dc=list(reversed(db))
 
sa=[]

def getsale():
    for b in range(0,36):
        print(data['mods']['itemlist']['data']['auctions'][b]['view_sales'])
        sa.append(int(str(data['mods']['itemlist']['data']['auctions'][b]['view_sales'][0:-3])))
       
getsale()

sb=sorted(sa)

sc=list(reversed(sb))

def fee():
    for c in range(0,36):
        if float(str(data['mods']['itemlist']['data']['auctions'][c]['view_fee']))==0.00:
            print('第'+str(c+1)+'件商品包邮')
        
fee()
