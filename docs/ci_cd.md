# CI/CD

## CI

- `flutter_test`によるユニットテスト
  - カバレッジは現状 0.9%  
    ![カバレッジ](./images/code_coverage.png)
  - 今後継続的にカバレッジを増やしていく
- GitHub Actions による CI
  - PR 作成・同期時、main マージ・プッシュ時、毎日 0 時

## CD

- fastlane
  - iOS
    - 証明書管理
    - Firebase App Distribution へのアップロード・配信
    - TestFlight へのアップロード・配信
  - Android
    - Play Store へのアップロード
- 今後 GitHub Actions による CD
