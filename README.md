# よりみちスタンド 配信カタログ / Yorimichi Stand Feed

VRChat ワールドギミック **「よりみちスタンド」** が読み込む静的カタログを配信するリポジトリです。

よりみちスタンドは、VRChat のワールド内で **アバターを選ぶと、そのアバターに対応した BOOTH の衣装・アクセサリーが並ぶ検索端末** です。データは [よりみちクローゼット](https://yorimichi.cc) の対応関係データベースから生成しています。

- 配信 URL: `https://yorimichi-closet.github.io/yorimichi-stand-feed/v1/`
- 更新: 日次バッチが生成し、`gh-pages` ブランチへ publish します

## 構成

| ブランチ | 中身 |
|---|---|
| `main` | この README とツール類（データは入れません） |
| `gh-pages` | 配信データ本体。**毎回 orphan ブランチとして作り直して force-push** します（同じファイル名で中身だけ差し替わるため、通常の履歴だと肥大するため） |

```
v1/
  index.json          目次（世代・掲載アバター一覧）
  a/NNN.json          アバター 1 体ぶんのアイテム一覧とファセット情報
  atlas/aNNN-M.jpg    サムネイル画像アトラス（2048x2048・256px グリッド）
```

`gh-pages` の直下には `.nojekyll` を置いています（Jekyll のビルドを止めるため）。

## なぜ GitHub Pages なのか

VRChat の Udon から取得できる URL は VRChat 側の許可ドメインに限られており、`*.github.io` はその筆頭です。VRChat 公式の画像読み込みサンプル（[vrchat-community/examples-image-loading](https://github.com/vrchat-community/examples-image-loading)）も同じ構成で GitHub Pages を使っています。

なお `raw.githubusercontent.com` は許可ドメインに **含まれていない** ため使えません。

## 注意

- カタログの内容は BOOTH 上の公開情報に基づいています。価格・公開状況は BOOTH 側が正です
- 本リポジトリおよび「よりみちスタンド」は BOOTH / pixiv とは関係のない、第三者による非公式なプロジェクトです
- 掲載に関するお問い合わせ: https://yorimichi.cc

---

運営: ひだまりデジタルワークス (Hidamari Digital Works)
