---
description: 開発環境のセットアップとポート開放
---

環境構築のために必要なコマンドを自動実行します。

// turbo-all

9. 必要なサーバー起動やポート開放コマンドを実行します。
```pwsh
[Console]::OutputEncoding = [System.Text.Encoding]::UTF8;
Write-Host "--- MHWilds-Site 開発環境セットアップ ---" -ForegroundColor Cyan

# 1. Windows Firewall のポート 3000 を開放（管理者権限が必要な場合があります）
# ※既に開放済みの場合はエラーが出ますが、続行されます。
Write-Host "[1/2] ポート 3000 の開放を確認/試行中..." -ForegroundColor Yellow
powershell -Command "Start-Process powershell -ArgumentList 'netsh advfirewall firewall add rule name=\"MHWilds-Site-3000\" dir=in action=allow protocol=TCP localport=3000' -Verb RunAs"

# 2. ローカルサーバーをポート 3000 で起動
Write-Host "[2/2] ローカルサーバー (Port 3000) を起動します..." -ForegroundColor Yellow
Write-Host "停止するにはこのターミナルを終了するか Ctrl+C を押してください。" -ForegroundColor Gray
npx -y serve -l 3000 .
```
