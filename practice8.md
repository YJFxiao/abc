# abc
abc

import urllib.request as r

for a in range(0,100):
    try:
        url='https://s.taobao.com/search?q=%E8%A3%99%E5%AD%90&imgfile=&js=1&stats_click=search_radio_all%3A1&initiative_id=staobaoz_20180719&ie=utf8&loc=%E5%8D%97%E6%98%8C&ajax=true&s={}'
        data=r.urlopen(url.format(44*a)).read().decode("utf-8","ignore")
        f=open('tmp2.txt','a',encoding='utf-8')
        f.write(str(data)+'\n')
        f.close()
    except Exception as err:
        print('爬取错误')
            
