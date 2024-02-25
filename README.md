# misskey-dqxpresence

Misskey の表示名に現在の職業とレベルを反映する Python スクリプト

## 設定ファイル .dqxpresence

ホームディレクトリに設置します。

```
{
    "id": 667538238772,
    "namebase": "おるどら",
    "misskey_token": "<アクセストークン>",
    "misskey_instance": "https://misskey.io"
}
```

id はマイページのソースを表示して `meta property="og:url"` のところに記述されている数字です。

```
	<meta property="og:url" content="https://hiroba.dqx.jp/sc/character/667538238772/"></meta>
```

また、マイページ全体の公開設定を『制限なしで公開』にしてください。

## ステータスファイル .mpresence

ホームディレクトリに作成されます。  
現在の職業とレベルを保存しています。

## 使い方

```
misskey-dqxpresence
```

表示名に現在の職業とレベルを `{namebase}＠{職業}{レベル}` (例: おるどら＠デスマスター130) のように反映します。  
前回実行時と同じ職業・レベルなら何もしません。

```
mastodon-dqxpresence set status
```

表示名を `{namebase}＠{status}` (例: おるどら＠ニラを包む皮を川に捨ててはいけない) にセットします。

```
mastodon-dqxpresence reset
```

表示名を `{namebase}` (例: おるどら) にリセットします。
