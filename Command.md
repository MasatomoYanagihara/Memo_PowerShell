# PowerShell

## メモ
- オンラインマニュアル「https://learn.microsoft.com/ja-jp/powershell/module/microsoft.powershell.management/?view=powershell-7.2」
- ディレクトリの区切りを示す記号は「/」ではなく「\」。（JISだと円マーク）
- PowerShellはコマンドの大文字・小文字を区別しない。
- パスを指定する際に、空白を含むものがある場合は「"」で囲む。（Linuxでも同じ）
  ```PowerShell
  cd "C:\Program Files\"
  ```

---
## コマンド

### Get-Help コマンド
ヘルプを表示する
Linux「コマンド --help」
```PowerShell
Get-Help Get-ChildItem
```

---
### EXIT
コンソールを終了する
Linux「exit」
```PowerShell
EXIT
```

---
### Get-ChildItem
今いるディレクトリに存在するファイル・ディレクトリを出力  
Linux「ls -l」  
```PowerShell
Get-ChildItem
```
パスを指定（C:\Program Files\）
```PowerShell
Get-ChildItem "C:\Program Files\"
```
ファイル名のみ出力  
Linux「ls -l」 
```PowerShell
Get-ChildItem -Name
```
再帰的に出力
```PowerShell
Get-ChildItem -Recurse
```

---
### Get-Location
カレントディレクトリを出力  
Linux「pwd」 
```PowerShell
Get-Location
```
---
### Set-Location
ディレクトリ移動  
Linux「cd」  
C:に移動
```PowerShell
Set-Location C:\
```
---
### New-Item -ItemType Directory
ディレクトリを作成  
Linux「mkdir」
```PowerShell
New-Item -ItemType Directory testdir
```

---
### Remove-Item
ファイルを削除  
Linux「rm」
```PowerShell
Remove-Item testfile
```

ディレクトリを削除  
Linux「rmdir」  
中身が空でなければ確認のプロンプトが表示される。  
```PowerShell
Remove-Item testdir
```

---
### Move-Item
ファイルやディレクトリを移動    
Linux「mv」  
testfileをdir1ディレクトリに移動
```PowerShell
Move-Item testfile .\dir1\
```

---
### Rename-Item
ファイルやディレクトリをリネーム
Linux「mv」
パス指定はできない
カレントディレクトリのItemのみ可
file1をfile2にリネーム
```PowerShell
Rename-Item file1 file2
```

---
### Copy-Item
ファイルやディレクトリをコピー
Linux「mv」
パス指定はできない
カレントディレクトリのItemのみ可
file1をfile2にリネーム
```PowerShell
Rename-Item file1 file2
```
