# abc
abc
def look():
    for d in range(0,36):
        print(data['mods']['itemlist']['data']['auctions'][d]['title'])
        print(data['mods']['itemlist']['data']['auctions'][d]['view_price'])
        print(data['mods']['itemlist']['data']['auctions'][d]['item_loc'])
        print(data['mods']['itemlist']['data']['auctions'][d]['view_sales'])
        if (d+1)%4==0:
            print('-'*20)
            continue
        if d==35:
            break
look()           
            
for e in sb:
    while e>=10000:
        print('销量很高，极受欢迎')
        break
    while e>=5000 and e<10000:
        print('销量不错，较受欢迎')
        break
    while e<5000:
        print('销量一般')
        break
