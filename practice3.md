# abc
abc
import urllib.request as r
data=r.urlopen("http://api.openweathermap.org/data/2.5/weather?q=nanyang&mode=json&units=metric&lang=zh_cn&APPID=6a67ed641c0fda8b69715c43518b6996").read().decode("utf-8","ignore")

import json
data=json.loads(data)

print("气温"+str(data["main"]["temp"]))
print("天气情况"+str(data["weather"][0]["description"]))
data["main"]["pressure"] 
