# abc
abc
url="http://api.openweathermap.org/data/2.5/forecast?q=zhengzhou,cn&mode=json&lang=zh_cn&&APPID=6a67ed641c0fda8b69715c43518b6996&units=metric"
import urllib.request as r
data=r.urlopen(url).read().decode("utf-8","ignore")

import json
data=json.loads(data)

def weather(a,b):
    print('第'+str(a)+'天')
    print('温度'+str(data["list"][b]["main"]["temp"]))
    print('天气情况'+str(data["list"][b]["weather"][0]["description"]))
    a=str(data["list"][b]["weather"][0]["main"])
    if a=='Clear':
        print('晴天')
    elif a=='Clouds':
        print('多云')
    elif a=='Rain':
        print('雨天')
        
weather(1,2)
weather(2,10)
weather(3,18)
weather(4,26)
weather(5,34)
