# Claude Code Task Commands

Claude Codeでタスクベースの開発を行うためのカスタムスラッシュコマンド集です。要件定義→詳細設計→ToDoリスト→実装を段階的に進めることで、品質の高いソフトウェア開発を支援します。

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

#### 1. **タスク環境準備** `/task-init`
```bash
/task-init your-task-name
```
- **機能**: 新しいタスクの環境準備と要件ヒアリング
- **用途**: プロジェクトの新機能開発や、課題対応の開始時
- **作成ファイル**: `.claude/tasks/{your-task-name}/`ディレクトリ構造

コマンド実行後、`init.md`ファイルに要件を簡潔に入力してください。この段階では、まだ詳細な要件定義は不要です。

#### 2. **要件定義作成** `/task-req`
```bash
/task-req your-task-name
```
- **機能**: 入力された要件から要件定義書を作成
- **用途**: 曖昧な要求を構造化された要件に変換
- **入力ファイル**: `.claude/tasks/{your-task-name}/init.md`
- **作成ファイル**: `.claude/tasks/{your-task-name}/requirements.md`

要件定義ファイル `requirements.md` が作成されます。必要に応じて修正してください。

#### 3. **詳細設計** `/task-design`
```bash
/task-design your-task-name
```
- **機能**: 既存システムを分析し、詳細設計を作成
- **用途**: 要件定義後の技術的設計
- **作成ファイル**: `.claude/tasks/{your-task-name}/design.md`

詳細設計ファイル `design.md` が作成されます。内容を確認し、必要に応じて修正してください。

#### 4. **ToDoリスト作成** `/task-todo`
```bash
/task-todo your-task-name
```
- **機能**: 詳細設計に基づく実装作業のタスクを分解
- **用途**: 開発作業の具体的な計画立案
- **作成ファイル**: `.claude/tasks/{your-task-name}/todo.md`

ToDoリストファイル `todo.md` が作成されます。内容を確認し、必要に応じて修正してください。

#### 5. **工数見積もり** `/task-estimate`
```bash
/task-estimate your-task-name
```
- **機能**: 要件定義・詳細設計・ToDoリストに基づく工数見積もり
- **用途**: 中級プログラマ（業務経験5年程度）が手作業で実装する場合の工数を算出
- **作成ファイル**: `.claude/tasks/{your-task-name}/estimate.md`

工数見積もりファイル `estimate.md` が作成されます。内容を確認し、必要に応じて修正してください。

#### 6. **開発実行** `/task-develop`
```bash
/task-develop your-task-name
```
- **機能**: ToDoリストに基づく段階的な実装
- **用途**: 実際の開発作業の実行

### ファイル構造

各タスクは以下の構造で管理されます：
```
.claude/tasks/{your-task-name}/
├── init.md         # 要件ヒアリング
├── requirements.md  # 要件定義
├── design.md       # 詳細設計
├── todo.md         # ToDoリスト
└── estimate.md     # 工数見積もり
```

## ライセンス

GPL-3.0 License

## 作者

Yuki Kokubo
