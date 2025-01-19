# SmartStudy Path 詳細設計書

## 1. API仕様
### ユーザー認証API
- POST /api/auth/login
- POST /api/auth/register

### 学習プランAPI
- GET /api/plans
- POST /api/plans
- PUT /api/plans/{id}

### 進捗管理API
- POST /api/progress
- GET /api/progress/report

## 2. データベース設計
### ユーザーテーブル
- id (PK)
- username
- password_hash
- role (student/parent)

### 学習プランテーブル
- id (PK)
- user_id (FK)
- subject
- target
- deadline

### 進捗テーブル
- id (PK)
- plan_id (FK)
- completed
- date

## 3. 画面遷移図
![画面遷移図](screen_flow.png)

## 4. コンポーネント詳細
### フロントエンド
- Reactコンポーネント構成
- 状態管理: Redux
- ルーティング: React Router

### バックエンド
- REST API設計
- 認証: JWT
- ロギング: Winston