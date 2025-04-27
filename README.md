# AWS × PHP‑FPM on ECS Boilerplate (Terraform)

🚧 **作成中 – Day 1 のスキャフォールド**

## このリポジトリについて
- **Terraform**：ステート管理 (S3 + DynamoDB) まで準備
- **ECS Fargate**：クラスタ・サービスは Day 6 で実装予定
- **CI/CD (GitHub Actions)**：Day 5〜8 で追加予定

## クイックスタート
```bash
# クローン
$ git clone <REPO_URL>
# Terraform 1.7.x をインストール（tfenv 推奨）
$ tfenv install 1.7.5 && tfenv use 1.7.5
# バックエンド初期化（infra/backend.tf のバケット名を自分用に変更）
$ cd infra && terraform init
```

## ロードマップ（抜粋）
| マイルストーン | 予定日 | 進捗 |
|----------------|--------|------|
| バックエンド設定 (S3/DynamoDB) | 2 日目 | ☐ |
| ネットワークモジュール作成 | 3 日目 | ☐ |
| Docker & ECR push | 4–5 日目 | ☐ |
| … | … | … |