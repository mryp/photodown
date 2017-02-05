FORMAT: 1A

# PhotoDown API

# Group 画像取得関連

## 画像一覧取得 [/api/list]
### POST

* 指定したページURLから画像のURLを抽出して返却する
* サイズ指定を行うとそのサイズ範囲内に合致した画像のみを返却する

+ Request (application/json)
    + Attributes
        + url: http://hogehoge.com/xxx/ (string, required) - ページURL
        + minwidth: 200 (number) - 最小幅
        + minheight: 400 (number) - 最小高さ
        + maxwidth: 2000 (number) - 最大幅
        + maxheight: 4000 (number) - 最小高さ

+ Response 200 (application/json)
    + Attributes
        + status: 0 (number) - 取得結果
        + images (array) - 画像情報リスト
            + (object)
                + image: http://xxx/zzz.jpg (string)
                + width: 300 (number)
                + height: 600 (number) 


## 画像一覧取得 [/api/list]
### POST