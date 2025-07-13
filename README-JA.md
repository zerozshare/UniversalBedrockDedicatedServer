# UBDSマネージャー v2.0.0
## Universal Bedrock Dedicated Server（プラグイン対応）

**バージョン**: 2.0.0  

---

## 🎯 UBDSとは？

UBDSは、Java Editionのサーバーのように、JARファイルから起動可能なMinecraft Bedrockサーバーを全OS（Windows、Mac、Linux）上で実行できるツールです。  
「plugins」フォルダに配置されたスタンドアロン形式のプログラムを同時に管理できます。

### 主な機能:
- ✅ Windows・Mac・LinuxでBedrockサーバーを起動
- ✅ Java製スタンドアロンプログラムの同時管理

---

## 📥 はじめに

### 必要要件:
- **Java 17以降**
- **PC**（Windows、Mac、Linux対応。CLIでも動作）

### クイックセットアップ:
1. リリースからUBDSをダウンロード
2. 任意のフォルダ（例: "MinecraftServer"）に配置
3. 次のコマンドで実行:  
   `java -jar Universal-BDS-2.0.0.jar`

---

## 📂 ファイル構成

UBDSマネージャーを実行すると、以下のフォルダ構成が自動的に生成されます:

    MinecraftServer/
    ├── Universal-BDS-2.0.0.jar     # UBDS本体
    ├── server.properties           # サーバー設定（ポートやワールド名など）
    ├── plugins/                    # プラグインフォルダ
    │   ├── MyBot/
    │   │   ├── MyBot.jar          # プラグイン本体
    │   │   └── config.yml         # プラグイン設定
    │   └── ChatManager/
    │       └── ChatManager.jar
    ├── logs/                       # ログファイル
    │   ├── latest.log              # 今日のログ
    │   └── 過去のログ…
    └── worlds/                     # ワールドデータ
        └── Bedrock level/

---

## 🎮 使い方

### サーバー起動方法:
1. `Universal-BDS-2.0.0.jar` を起動
2. 起動完了まで待機
3. サーバーが起動され、接続可能になります
4. MinecraftクライアントからIPで接続できます

### 基本コマンド:

#### サーバー管理（「!」で始まる）:
    !status     # サーバーの状態確認
    !info       # コンピュータの情報表示
    !plugins    # プラグイン一覧を表示
    !stop       # サーバー停止・プログラム終了
    !help       # コマンド一覧表示

#### プラグイン操作（「@」で始まる）:
    @プラグイン名 コマンド

例:
    @MyBot help           # MyBotプラグインのヘルプ
    @ChatManager reload   # ChatManagerを再読み込み

#### Minecraftサーバーへの直接コマンド（そのまま入力）:
    say こんにちは！         # 全プレイヤーにメッセージ送信
    list                  # プレイヤー一覧表示
    gamemode creative Steve  # Steveをクリエイティブに変更
    time set day          # 昼に時間設定

---

## 🔌 プラグイン追加方法

### ステップ1: プラグインを用意
- JARファイル（例: MyBot.jar）を入手
- スタンドアロン形式で動作するものに限る

### ステップ2: インストール
- JARファイルを "plugins" フォルダに配置
- 例: "plugins/MyBot.jar" にコピー

### ステップ3: サーバー再起動
- プラグインが自動起動します
- エラーが出たら再度再起動してください

### ステップ4: 利用開始
- 例: `@MyBot help` を入力
- プラグインごとにコマンドが異なります

---

## 🔧 主な設定

### サーバー設定の変更:
"server.properties" ファイルを編集:

    server-name=My Awesome Server    # サーバー名
    gamemode=survival               # 初期ゲームモード
    difficulty=easy                 # 難易度
    max-players=20                  # 最大プレイヤー数
    server-port=19132               # ポート番号（必要に応じて変更）

### プラグイン設定の変更:
各プラグインには個別の設定ファイルがあります:
- MyBot: "plugins/MyBot/config.yml"
- ChatManager: "plugins/ChatManager/settings.json"

---

## ❓ トラブルシューティング

### 問題: サーバーが起動しない
**対処法:**
1. ポート19132が使用可能か確認
2. エラーメッセージ確認
3. `!info` コマンドでシステム情報確認

### 問題: プラグインが動かない
**対処法:**
1. `!plugins` で実行中か確認
2. Javaがインストールされているか確認: `java -version`
3. "logs/latest.log" を確認

### 問題: 接続できない
**対処法:**
1. "server.properties" でポート確認
2. ファイアウォール設定確認
3. IPアドレスとポートを友人に伝える

### 問題: サーバーが重い
**対処法:**
1. 他のアプリケーションを終了
2. 不要なプラグインを削除
3. server.propertiesで max-players を減らす

---

## 📋 クイックリファレンス

### コマンドの種類:
- **!コマンド** = サーバープログラム管理用
- **@プラグイン名 コマンド** = プラグインと通信
- **通常コマンド** = Minecraftサーバーへの直接操作

### よく使うコマンド:
    !status          # サーバー状態確認
    !plugins         # プラグイン一覧表示
    say Hello!       # 全体チャット
    list             # オンラインプレイヤー確認

---

## 📞 サポート

**開発者**: ZSHARE  
**バージョン**: 2.0.0  

**お問い合わせの際は以下をお知らせください:**
- OS（Windows, Mac, Linux）
- "latest.log" 内のエラー内容
- 実行しようとした操作内容
- サポートは https://discord.zpw.jp にて受付中
