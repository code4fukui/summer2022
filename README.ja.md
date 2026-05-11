# summer2022

深野さんとの共同制作として作成された、地図ベースのデータ収集および可視化ツールのプロトタイプです。

## デモ

- **ふくモン プロトタイプ (Full Survey):** [mysurvey.futbol/fukumon](https://www.mysurvey.futbol/fukumon)
- **マップビューのみ:** [code4fukui.github.io/summer2022/](https://code4fukui.github.io/summer2022/)

## 概要

このプロジェクトでは、`<csv-map>` Webコンポーネントを使用し、HTMLファイルに埋め込まれたCSVデータから直接、地図上にPOI（関心地点）を描画します。CSVの各行は1つの地点を表し、タイトル、画像URL、および `geo3x3` 位置コードが含まれます。

地図上には、漆器職人（`土直漆器さん`）や古生物学者（`化石学者さん`）など、地元の人物や職人のデータポイントが、さまざまなプラットフォームから取得した画像とともに表示されます。

## 使い方

地図を実装するには、`csv-map.js` スクリプトを読み込み、HTML内に `<csv-map>` 要素を追加してその中にデータを記述します。

**例:**
```html
<script type="module" src="https://code4fukui.github.io/csv-map/csv-map.js"></script>

<csv-map>
title,url,filename,geo3x3
深野さん,https://scontent-sjc3-1.xx.fbcdn.net/v/t1.18169-9/..._n.jpg,13265979..._n.jpg,E913873235844
土直漆器さん,https://drive.google.com/file/d/1v2KcxfeGGbRI8m7Qh1n79taz_Az2AP6Z/view,職人_漆器.jpeg,E9138733613632
</csv-map>
```

### CSVデータ形式

CSVデータには以下の列を含める必要があります。

- `title`: マップピンの名前またはタイトル。
- `url`: 画像または関連するWebページへの直接URL。
- `filename`: 画像のファイル名。
- `geo3x3`: `geo3x3` 位置コード。
