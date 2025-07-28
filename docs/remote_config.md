# [Firebase Remote Config](https://firebase.google.com/docs/remote-config?hl=ja)

> Firebase Remote Config は、ユーザーにアプリのアップデートをダウンロードするよう依頼しなくても、クライアント アプリまたはサーバーの動作や外観を変更できるクラウド サービスです。

## 主な用途

- アップデート推奨・強制アップデート
  - アプリ起動時に現在のバージョンを、Remote Config上の推奨バージョンと照らし合わせる
  - 推奨バージョンでない場合は、アップデートを促す
  - 強制アップデートが必要な場合は、全ての機能を無効化し、アプリストアに移動
- 各種 URL
  - ソースコードに埋め込むのではなく、Remote Configの値を使うように実装を変更
- Feature Flag と A/B テスト
  - Funchや新しいデザインシステムを段階リリース
