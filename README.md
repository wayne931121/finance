# finance
使用不同頻率分析股票 stock analysis at different frequency

https://colab.research.google.com/drive/1NUq1BkDY0gKqSmz_2Ib7IMYNdARVHVfl?usp=drive_link

這個程式會將股票紀錄用yfinance抓下來，一天一筆資料，每筆資料紀錄值為開盤價加收盤價再除以二。
This program will use yfinance module to capture stock records, and transfers to datas, and the value of data record is the (open+close)/2 per day.

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

```
30:頻率週期為每30筆資料分析一次

['2024-04-30', '2024-06-13', '2024-07-24'] 0-01-12 144.78333333333333

('2024-06-13'到'2024-07-24'的價格加總平均 減掉 '2024-04-30'到'2024-06-13'的價格加總平均) 再除以資料筆數 等於 144.78333333333333

'2024-04-30'到'2024-07-24'日期區間除以二 等於 0年-01月-12天

0-01-11~18 每0個年1個月11~18天 分析一次
```

```
30:
 Analyzed once every 30 pieces of datas

['2024-04-30', '2024-06-13', '2024-07-24'] 0-01-12 144.78333333333333

(The summed average price from '2024-06-13' to '2024-07-24' minus the summed average price from '2024-04-30' to '2024-06-13') Then divided by the number of data items Equal to 144.783333333333333

The date range from '2024-04-30' to '2024-07-24' divided by two equals 0 years - 01 months - 12 days "0-01-12"

0-01-11~18 Analyze every 0 years, 1 month, 11~18 days
```
