# CI/CD

## CI

> Continuous Integration（継続的インテグレーション）の略。

- 昨年度まで
  - ユニットテストケースが存在しない
  - ソースコードの品質を保証できない
- 今年度から
  - CIワークフローを構築
  - コードの品質を保証できる環境を構築

### やったこと

- `flutter_test`によるユニットテスト
  - テストコードがどの程度の実装をカバーしているかを表すテストカバレッジは現状 0.9%  
    ![カバレッジ](./images/code_coverage.png)
  - 今後継続的に増やしていく
- GitHub Actions による CI
  - トリガー
    - PR 作成・同期時
    - main マージ・プッシュ時
    - 毎日 0 時

## CD

> Continuous Delivery（継続的デリバリー）の略。

- 昨年度まで
  - リリース前に手動でテスト環境へデプロイ
- 今年度から
  - CDワークフローの構築を目指し、fastlaneを用いて配信を自動化

### やったこと

- fastlane
  > fastlane is an open source platform aimed at simplifying Android and iOS deployment. fastlane lets you automate every aspect of your development and release workflow.
  - iOS
    - 証明書管理
    - Firebase App Distribution へのアップロード・配信
    - TestFlight へのアップロード・配信
  - Android
    - Play Store へのアップロード
- 今後 GitHub Actions による CD
