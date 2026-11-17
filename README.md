# 転職活動の管理アプリ

## 技術スタック

### フロントエンド

- Next.js, TypeScript
- TailwindCSS
- shadcn/ui
- dnd kit

### バックエンド

- Hono
- Drizzle
- Better Auth

## DB設計案

### companies

企業テーブル

- id
- user_id
- name
- url
- created_at
- updated_at

### applications

応募テーブル

- id
- company_id
- user_id
- job_title
- job_url
- status
  - 気になる
  - カジュアル面談
  - 書類選考
  - 一次面接
  - 二次面接
  - 最終面接
  - 内定
  - 辞退
  - 不合格
- salary_min
- work_style
- memo
- applied_at
- created_at
- updated_at

### interviews

面接テーブル

- id
- application_id
- user_id
- scheduled_at
- reflection
- created_at
- updated_at

### interview_questions

面接で聞かれた質問と回答のテーブル

- id
- interview_id
- user_id
- question
- answer
- created_at
- updated_at

### users

ユーザーテーブルは作らない。Better Auth のuser.id を使用する？
