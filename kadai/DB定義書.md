# DB定義書

### ER図
[ER図はこちら](https://github.com/Aso2001041/2021sys-design/blob/main/ER%E5%9B%B3.md)

##　データベース詳細
### d_purchase
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|オーダーID|order_id|bigint(20)|Y|Y|-|
|顧客コード|custmor_code|varchar(50)|-|Y|-|
|購入日|purchase_date|date|-|Y|-|
|総額|total_price|int(11)|-|Y|-|


### d_purchase
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|詳細ID|detail_id|bigint(20)|Y|Y|-|
|オーダーID|order_id|bigint(20)|Y|Y|Y|
|商品コード|item_code|int(11)|-|Y|-|
|価格|price|int(11)|-|Y|-|
|数量|num|int(11)|-|Y|-|

### m_customers
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|顧客コード|custmer_code|varchar(50)|Y|Y|-|
|パスワード|pass|varchar(50)|Y|Y|Y|
|氏名|name|varchar(20)|-|Y|-|
|住所|addres|varchar(100)|-|Y|-|
|電話番号|tel|varchar(20)|-|Y|-|
|メールアドレス|mail|varchar(100)|-|Y|-|
|削除フラグ|del_flag|int(11)|-|-|-|
|登録日|reg_date|date|-|Y|-|


### m_items
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|カテゴリ|category_id|int(11)|Y|Y|-|
|氏名|name|varchar(20)|-|Y|-|
|登録日|reg_date|date|-|Y|-|

### m_category
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|商品コード|item_code|int(11)|Y|Y|-|
|商品名|item_name|varchar(50)|-|Y|-|
|価格|price|int(11)|-|Y|-|
|カテゴリID|category_id|int(11)|-|Y|Y|
|画像ファイル名|image|varchar(200)|-|Y|-|
|詳細説明|dtail|varchar(500)|-|-|-|
|削除フラグ|del_flag|int(11)|-|-|-|
|登録日|reg_date|-|-|Y|-|
