# Claude Code Task Commands

Claude Codeでタスクベースの開発を行うためのカスタムスラッシュコマンド集です。要件定義から詳細設計、ToDoリスト作成、実装までを段階的に進めることで、品質の高いソフトウェア開発を支援します。

## インストール

1. このリポジトリをクローンします：
```bash
git clone https://github.com/tombolo-jp/claude-code-task-commands.git
```

2. Claude Codeのコマンドディレクトリにファイルをコピーします：
```bash
cp claude-code-task-commands/*.md ~/.claude/commands/
```

## 使用方法

### 基本的なワークフロー

#### 1. **要件定義** `/task-init`
```bash
/task-init your-task-name
```
- **機能**: 新しいタスクの環境準備と要件ヒアリング
- **用途**: プロジェクトの新機能開発や、課題対応の開始時
- **作成ファイル**: `.claude/tasks/{task_name}/requirements.md`

コマンド実行後、作成された要件定義ファイル `requirements.md` を直接編集し、具体的な要件を記載してください。

#### 2. **詳細設計** `/task-design`
```bash
/task-design your-task-name
```
- **機能**: 既存システムを分析し、詳細設計を作成
- **用途**: 要件定義後の技術的設計
- **作成ファイル**: `.claude/tasks/{task_name}/design.md`

詳細設計ファイル `design.md` が作成されます。内容を確認し、必要に応じて修正してください。

#### 3. **ToDoリスト作成** `/task-todo`
```bash
/task-todo your-task-name
```
- **機能**: 詳細設計に基づく実装作業のタスクを分解
- **用途**: 開発作業の具体的な計画立案
- **作成ファイル**: `.claude/tasks/{task_name}/todo.md`

ToDoリストファイル `todo.md` が作成されます。内容を確認し、必要に応じて修正してください。

#### 4. **開発実行** `/task-develop`
```bash
/task-develop your-task-name
```
- **機能**: ToDoリストに基づく段階的な実装
- **用途**: 実際の開発作業の実行

### ファイル構造

各タスクは以下の構造で管理されます：
```
.claude/tasks/{your-task-name}/
├── requirements.md  # 要件定義
├── design.md       # 詳細設計
└── todo.md         # ToDoリスト
```

## ライセンス

GPL-3.0 License

## 作者

Yuki Kokubo
