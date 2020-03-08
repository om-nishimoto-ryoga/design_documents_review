# テーブル定義書2(問題抽出)
## 全体
- テーブルごとにシートが分かれていない
- テーブル名の命名規則が不適切
    - 小文字複数形スネークケースで命名
- idがないテーブルが存在する
    - テーブル名_idとしなくていい
- 入荷テーブルがない
    - 入荷は商品の入荷を管理するため

## admins
- admin_idにindexがない
- カラム名にテーブル名の接頭辞がある
    - admin_email, admin_passwordのadmin_は不要

## users
- カラム名に省略形を使用すべきではない
    - user_l_nameなど
- member_statusだとfalseの状態が何を示すかわからない

## ships
- ship_idにindexがない
- ship_name, ship_address, ship_tel, ship_codeのship_は不要

## products
- 在庫ステータスと在庫数は不要
    - 在庫ステータスは在庫数から判別して表示する
    - 在庫数は入荷テーブルと受注詳細テーブルから算出可能

## discs
- disc_numのdisc_は不要
- products_idではなく、product_id

## songs
- songカラムの命名が不適切
    - songが曲名だと分かりづらい

## labels
- labelカラムの命名が不適切
    - labelがレーベル名だと分かりづらい

## artists
- artistカラムの命名が不適切
    - artistがアーティスト名だと分かりづらい

## genres
- genreカラムの命名が不適切
    - genreがジャンル名だと分かりづらい

## cart items
- テーブル名の命名規則が不適切
    - 小文字複数形スネークケースで命名
- products_idではなく、product_id
- buy numが不適切
    - カラム名に空欄がある
    - 購入枚数は数量を表す名称にすべき

## sell
- payカラムの命名が不適切
    - 支払い方法だとわからない
- totalカラムの命名が不適切
    - なんのtotalかわからない
- sell_detailsとのリレーションが逆

## sell_details
- 購入時の価格を保持するカラムがない
- 商品idがFKになっていない

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
