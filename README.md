# ctf-tools
https://github.com/yoshihito-tatano/ctf-tools.git

# CTFツールまとめ

# 共通

| ツール/コマンド | 説明/メモ | オプション | 参考 |
| --- | --- | --- | --- |
| base64 | 英数字と３種類の記号(+=/）のみで文字列に変換するもの |  |  |
| nmap |  | -n -sV |  |
| ASCII |  |  |  |
| wget |  | -r -np |  |
| grep |  | -r  |  |
| file |  |  |  |
| strings |  |  |  |
| exiftool |  |  |  |
| objdump |  | -d |  |
| vim |  | :%!xxd |  |
| unzip |  | -P {password} |  |
| pdftotext |  | -opw {password} pdf.file |  |
| nc |  | -lp |  |
| socat |  |  |  |
| sageMath | apt-get install sagemath |  |  |
|  |  |  |  |

# Network

# Web/SQL

| ツール/コマンド | 説明/メモ | オプション | 参考 |
| --- | --- | --- | --- |
| Burp Suite |  |  |  |
| wget |  | -r -np |  |
| sqlmap |  |  |  |
| CSP Evaluator | Content Security Policyのチェックが可能 |  | https://csp-evaluator.withgoogle.com/ |
|  |  |  |  |
|  |  |  |  |

dump.sql

API Tools
postman

[Postman API Platform | Sign Up for Free](https://www.postman.com/)

sql injection cheat seat

[SQL Injection Cheat Sheet | Invicti](https://www.invicti.com/blog/web-security/sql-injection-cheat-sheet/)

xss cheat seat

[https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html](https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html)

# FORENSIC

| ツール/コマンド | 説明/メモ | オプション | 参考 |
| --- | --- | --- | --- |
| Burp Suite |  | DecoderでBase64の相互変換ができる |  |
| wget |  | -r -np |  |
| volatility3 |  | python3 http://vol.py -f メモリダンプファイル プラグイン [プラグインパラメータ]
python3.7 http://vol.py -f {file.mem} windows.pstree > ./test.txt

windows.cmdline
windows.registry.printkey —key “Software¥Microsoft¥Windows¥currentVersion¥Run” | 通常、ユーザ権限で起動するプロセスはexplorer.execの個プロセスになる |

ファイルシグネチャ

バイナリエディタ　GHex -C

# BINARY

| ツール/コマンド | 説明/メモ | オプション | 参考 |
| --- | --- | --- | --- |
| Burp Suite |  |  |  |
| wget |  | -r -np |  |
| IDA | reversing |  | https://hex-rays.com/ida-free/ |
| z3 | reversing |  |  |
| angr | reversing |  |  |
| objdump |  |  |  |
| strace |  |  |  |
| xxd |  |  |  |
| nm |  |  |  |
| ldd |  |  |  |
| setarch -R |  |  |  |

# PWN/CRYPT

| ツール/コマンド | 説明/メモ | オプション | 参考 |
| --- | --- | --- | --- |
| zbaring |  |  |  |
| openssl  |  | -pubout 秘密鍵から公開鍵の生成
-pubin 公開鍵のパラメータ確認
rsautl -encrypt -inkey -pubin -in　RSA鍵でファイルの暗号化/復号 |  |
| john the ripper |  | unshadow shadow > hash.txt
john hash.txt
john -format=crypt —wordlist={file}
zip2john file.zip > hash.txt
perl http://pdf2john.pl {file} > hash.txt |  |
| quipqiop | 単一換字式暗号を解読する |  | https://quipqiup.com/ |
| hashcat | ハッシュに対する高速な総当たり攻撃を実施する | hashcat -a  3 -m 100 hash__data —show
-a:探索アルゴリズム、-m:総当たり回数 |  |
| hashpump | Length Extension Attackのツール
CRC32、MD5、SHA-1、SHA-256、SHA-512への攻撃が有効 | hashpump | https://github.com/bwall/HashPump |
| YAFU | 素因数分解ツール |  | https://sourceforge.net/projects/yafu/ |
| primefac/fork | 素因数分解ツール |  | https://github.com/elliptic-shiho/primefac-fork |
| peda | gdb機能を拡張するスクリプト |  | https://github.com/longld/peda |
| gef | x86, arm以外も可　gdb機能拡張 |  | https://github.com/hugsy/gef |
| pwndbg |  |  | https://github.com/pwndbg/pwndbg |
| Pwngdb(angelheap) | ヒープ管理や各チャンクの状態を可視化 |  | https://github.com/scwuaptx/Pwngdb |
| nasm | x86アセンブラ |  | https://github.com/netwide-assembler/nasm |
| pwntools |  | pip3 install pwntools | https://github.com/Gallopsled/pwntools |
| seccomp tools | seccompフィルタ解析を補助するツール。実行バイナリからフィルタの列挙や読みやすい形式にアセンブル、逆アセンブルが可能 |  | https://github.com/david942j/seccomp-tools |
|  |  |  |  |
