# DataFrame

### pd.datafram(data)
data is like list of dict they conver intp row/column

```bash
data = [
  {"SKU": "...", "Size": "...", "Color": "...", "QTY": 2},
  {"SKU": "...", "Size": "...", "Color": "...", "QTY": 1},
  ...
]
```
    csv/excel by panda datafream

        ORD  QTY       Size        Color                        SKU
    0    3    1  Free Size         Pink  LIQUID SOAP DISPENSER-1AA
    1    1    1  Free Size         Blue   LIQUID SOAP DISPENSER-1B
    2    2    1  Free Size        White   LIQUID SOAP DISPENSER-1E
    3    1    1  Free Size  Multicolour   LIQUID SOAP DISPENSER-1G
    4   28    1  Free Size  Multicolour   LIQUID SOAP DISPENSER-1K
    5    3    2  Free Size  Multicolour   LIQUID SOAP DISPENSER-1K
    6    1    1  Free Size         Pink               MARK-PINK[C]


# size 

Count number of rowes somting like above example index number (0,1,2..)

# reset_index() & reset_index(name='ORD') 

reset_index = onverts the grouped keys (SKU, Size, Color, QTY) into columns
name = 'ORD' means -> renames the counts column to ORD


# sort_values
```bash
    .sort_values(['SKU','Size','Color','QTY'])
    
    -> Sorts the final table so similar SKUs come together.
```