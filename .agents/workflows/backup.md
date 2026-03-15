---
description: 作業内容のバックアップを作成します
---
作業終了時に、プロジェクト全体をZIPにまとめてバックアップを作成します。

// turbo-all

1. バックアップ作成スクリプトを実行します。
```pwsh
[Console]::OutputEncoding = [System.Text.Encoding]::UTF8;
Write-Host "--- バックアップ作成開始 ---" -ForegroundColor Cyan
& "e:\Users\tai_r\Documents\AI\mhwilds-site\scripts\create_backup.ps1"
```
