# finance
## 使用不同頻率分析股票 stock analysis at different frequency
https://finance.yahoo.com/

https://colab.research.google.com/drive/1NUq1BkDY0gKqSmz_2Ib7IMYNdARVHVfl?usp=drive_link

這個程式會將股票紀錄用yfinance抓下來，一天一筆資料，每筆資料紀錄值為開盤價加收盤價再除以二。
This program will use yfinance module to download stock records, and transfers to datas, and the value of data record is the (open+close)/2 per day.

```
name = "stock name"
b = average(name)
fin(30)

Output:
30
['2023-09-13', '2023-10-30', '2023-12-08'] 0-01-13 28.2
['2023-10-30', '2023-12-11', '2024-01-22'] 0-01-11 21.033333333333335
['2023-12-11', '2024-01-23', '2024-03-14'] 0-01-17 106.58333333333333
['2024-01-23', '2024-03-15', '2024-04-29'] 0-01-18 89.4
['2024-03-15', '2024-04-30', '2024-06-12'] 0-01-14 55.35
['2024-04-30', '2024-06-13', '2024-07-24'] 0-01-12 144.78333333333333
```

## Simply
```
['2024-04-30', '2024-06-13', '2024-07-24'] 0-01-12 144.78333333333333

2024年4月30日至2024年7月24日股票價值正向，價值指標上漲144.78333333333333，兩個時間中點座標經過時間0年-01月-12天
The stock value from 2024-04-30 to 2024-07-24 is positive and value index up 144.78333333333333, duration of midpoint is 0y-01m-12d

(2024年4月30日至2024年7月24日股票價值正向，平均每筆資料上漲144.78333333333333，時間週期大約是0年-01月-12天)
```

## Explain
```
Output:
30
['2023-09-13', '2023-10-30', '2023-12-08'] 0-01-13 28.2
['2023-10-30', '2023-12-11', '2024-01-22'] 0-01-11 21.033333333333335
['2023-12-11', '2024-01-23', '2024-03-14'] 0-01-17 106.58333333333333
['2024-01-23', '2024-03-15', '2024-04-29'] 0-01-18 89.4
['2024-03-15', '2024-04-30', '2024-06-12'] 0-01-14 55.35
['2024-04-30', '2024-06-13', '2024-07-24'] 0-01-12 144.78333333333333

30:頻率週期為每30筆資料分析一次 Analyzed once every 30 pieces of datas (data period)

Output Item:"""['2024-04-30', '2024-06-13', '2024-07-24'] 0-01-12 144.78333333333333"""

['2024-04-30', '2024-06-13', '2024-07-24'], 144.78333333333333
2024-06-13到2024-07-24的平均價格 減掉 2024-04-30到2024-06-13的平均價格 再除以資料週期筆數 等於 144.78333333333333
The average price from 2024-06-13 to 2024-07-24 minus the average price from 2024-04-30 to 2024-06-13, then divided by the number of data period is equal to 144.783333333333333

0-01-12
'2024-04-30'到'2024-07-24'日期區間除以二 等於 0年01月12天
The days from 2024-04-30 to 2024-07-24 divided by two equals to 0 years - 01 months - 12 days "0-01-12"

0-01-11~18 每0個年1個月11~18天 分析一次
0-01-11~18 Analyze every 0 years, 1 month, 11~18 days
```
