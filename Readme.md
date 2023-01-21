# Vagrant * Docker * PHPの環境構築
### 参考
- https://techblog.istyle.co.jp/archives/6559

### Docker上のindex.phpを開こうとしたが403エラー
- 事象：403 forbidden
- 解決：https://teratail.com/questions/349722
    - apacheのデフォルトルートは/var/www
    - ここにindex.php, index.htmlがなかったので何もしない
    - 次に/var/wwwの一覧を表示しようとしたがデフォルトでは権限が制約されているのでできない

### Xdebugの使いかた
- 1, SSH RemoteでVagrant内のVSCODEを起動
- 2, 1,で起動したVSCODEからphpコンテナへREMOTEアクセス
- 3, PHP DEBUGをインストール
- デバッグできる状態になる