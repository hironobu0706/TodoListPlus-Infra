Todoリスト（ポートフォリオ）の環境構築手順を記載します。
必要なリポジトリは3つ

1. インフラ、DB：todoVueJavaInfra(このリポジトリ)
2. フロント　　：https://github.com/hironobu0706/TodoListPlus-Front
3. バック　　　：https://github.com/hironobu0706/TodoListPlus-Back

## 必要なソフト
+ docker及びdocker-compose
+ git


## 手順
1.上記3リポジトリを任意のフォルダにクローンする。 ※必ず同じフォルダに配置すること。  
↓のイメージ（2階層目まで表示）
```
TodoListPlus
├─TodoListPlus-Back
│ ├─.mvn
│ ├─.settings
│ ├─src
│ └─target
├─TodoListPlus-Front
│ ├─.vscode
│ ├─node_modules
│ ├─public
│ └─src
└─TodoListPlus-Infra
├─initdb.d
└─mysql_data
```

2.TodoListPlus-Infraフォルダの直下でターミナルを開く

3.docker-compose up -d --build　を実行  
※もし失敗した場合すべてのフォルダを削除し、1からやり直し

4.docker-compose ps -a を実行し、ステータスがupになっていることを確認する。  
※もしupではない場合 docker-compose down を実行し再度3の手順を実行する。何度かやってみて解決しなければすべてのフォルダを削除し、1からやり直し

5.ブラウザで  
```http://localhost:5173/```  
にアクセスしトップページ画面が表示されれば環境構築成功
<img width="1558" height="651" alt="image" src="https://github.com/user-attachments/assets/cc91cb5c-2c5c-47aa-9ea0-7c6a3f592dd4" />

