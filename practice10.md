# abc
abc

ls=open('all_school.txt',encoding='utf-8').readlines()
schoolls=[]

for line in ls:
    schoolls.append(line.split('-jianjie-')[1].split('.')[0])
    
import urllib.request as r
url='http://www.gaokaopai.com/university-ajaxGetMajor.html'
headers={'User-Agent':' Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36',
         'X-Requested-With': 'XMLHttpRequest'}

f=open('海南招生人数.txt','a',encoding='utf-8')
for schoolid in schoolls:
    for kemu in [1,2]:
        
        try:
            req=r.Request(url,data='id={}&type={}&city=46&state=1'.format(schoolid,kemu).encode(),headers=headers)
            f.write(r.urlopen(req).read().decode('utf-8','ignore')+'\n')
            print(schoolid+"爬虫成功")
        except Exception as err:
            print('爬取错误')
f.close()

ls2=open("XML高考派城市.txt",encoding='gbk').readlines()
cityid=[]
for line in ls2:
    cityid.append(line.split(', ')[1].split(')')[0])
