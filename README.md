# 簡単な Websocket アプリ

## サーバーの起動
```
node index.js
```

## クライアントから接続(development tool から実行できる)
```
// サーバーに ws プロトコルで接続
let ws = new WebSocket("ws://localhost:8080")

// サーバーからもらったデータをログに出力
ws.onmessage = message => console.log(`We received a message from server ${message.data}`)

// サーバーにデータを送る
ws.send("クライアントから送ったデータ")

// 接続を閉じる
ws.close()
```

