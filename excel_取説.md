# Excelでできること
## 重複チェック
+ 式（例）```=IF(COUNTIF(H:H,H1)>1,"重複あり","")```
+ 解説：範囲（H:H）の中に文字列（H1）のセルの内容と一致しているセルが2つ以上あるか判定できる。2つ以上ある場合は、重複ありと表示される。無い場合は何も表示されない。　

## ある文字列に特定の文字が含まれている個数を取得
+ 式（例）```=LEN(A1)-LEN(SUBSTITUTE(A2,B2,""))```
+ 解説：文字列（A2）のセル内に文字列（B2）のセルの内容がいくつ含まれているかチェックできる。B2の値を/や&等に変更すれば/や&の個数が取得できる

## 文字列の長さを取得
+ 式（例）```=len(A1)```
+ 解説：文字列（A1）のセルの内容の何文字なのか取得できる。文字列なので、英語でも日本語でも1文字は1文字として取得できる。

## ある文字列が指定された範囲に存在するかチェック
+ 式（例）```=vlookup(A1,A:B,2,false)```

+ 解説：文字列（A1）がA列に存在（完全一致）するかチェックする。完全一致するときは、Bの値が表示される。存在しない場合は、#N/Aが表示される。

## 英語をAからZまで並べる
+ 式（例）```=CHAR(CODE(E1)+1)```

## セルの値が含まれているかチェック
+ 式（例）```=COUNTIF(H2,"*"&E2&"*")```

## 偶数行のセルの色を決める
+ 式（例）```=MOD(ROW(),2)=0```

----
+ 式（例）```=IF(OR(A2>=80,B2>=80),"合格","不合格")」```

## 漢字等のルビを表示
+ 式（例）```=PHONETIC(A2)```

## 特定条件内の特定文字列の個数を調べる
+ 式（例）```=COUNTIFS(C3:C26,"○",D3:D26,"○")/COUNTIF(C3:C26,"○")```

