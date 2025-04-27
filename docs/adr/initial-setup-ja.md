# 🚀 AWS × PHP‑FPM on ECS – 初期リポジトリ設計（日本語版）

---

## 1. 目的

2 週間ロードマップ **Day 1** で作成する **空リポジトリ** と **GitHub Project ボード** の雛形を定義します。実際のコーディングや CI 設定は後続の日程で追加していきます。

---

## 2. 推奨ディレクトリ構成（空フォルダのみ）

```text
repo-root/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── feature_request.md  # 追加予定のテンプレート
│   └── workflows/              # CI 用ワークフロー（後日追加）
├── infra/                      # Terraform 一式
│   └── modules/                # 共通モジュール配置場所
└── docs/
    └── adr/                    # Architectural Decision Records
```

💡 **Day 1 では上記フォルダと `README.md`・`LICENSE` だけコミットしておけば OK** です。

---

## 3. `README.md` 初期スケルトン

````markdown
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
````

## ロードマップ（抜粋）

| マイルストーン                 | 予定日   | 進捗 |
| ------------------------------ | -------- | ---- |
| バックエンド設定 (S3/DynamoDB) | 2 日目   | ☐    |
| ネットワークモジュール作成     | 3 日目   | ☐    |
| Docker & ECR push              | 4–5 日目 | ☐    |
| …                              | …        | …    |

````

---
## 4. GitHub Project ボード構成
| カラム | 役割説明 |
|--------|-----------|
| **Backlog** | 未着手タスク。Day タスクを Issue 化して格納。 |
| **In Progress** | 作業中タスク。1 人 2〜3 枚推奨。 |
| **Review** | PR 提出後、レビュー待ち状態。 |
| **Done** | `main` ブランチにマージ済み。

**設定手順**
1. GitHub → *Project (Beta)* → *Board* を作成し、上記 4 カラムを追加。
2. 「Automation」設定で Backlog への新規 Issue 自動追加を有効化。
3. カスタムフィールド `Day` (数値) を追加し、ロードマップ追跡しやすくする。

---
## 5. Issue #1 — スコープ確定テンプレート
```markdown
### 🎯 目的
本リポジトリの Day 1〜14 スコープと Done の定義を確定する。

### ✅ Done の定義
- [ ] `README.md` に 2 週間ロードマップ表を含める
- [ ] GitHub Project ボードを作成し、カラムを Backlog / In Progress / Review / Done に設定
- [ ] Day 1〜14 の各タスクを Issue として Backlog に作成
- [ ] `.github/ISSUE_TEMPLATE/feature_request.md` を追加（テンプレ参照）

### 📄 追加情報
詳細なタスクは `/docs/roadmap-day1-14.md`（後日コミット予定）を参照してください。
````

---

## 6. 参考リンク

- GitHub Projects　ドキュメント: <https://docs.github.com/ja/issues/planning-and-tracking-with-projects/learning-about-projects>
- ADR パターン: <https://adr.github.io/>

---

## 7. 次のステップ

1. **このドキュメントを初回コミットに含めてリポジトリを公開**。
2. Project ボードと Issue 登録を完了すると **Day 1 ミッション達成** です。
