## useful tool
### du 檔案工具
|du|||
|:-:|:-:|:-:|
|-s|summary|顯示該目標的總用量，不顯示子目錄|
|-h|human readable|以磁碟單位顯示空間用量|
|--max-depth=N||限制只顯示至第N層子目錄|
### df 磁碟分割區工具
|df|||
|:-:|:-:|:-:|
|-h|human readable|以磁碟單位顯示空間用量|

### dd
|dd||
|:-:|:-:|
|if=FILE|指定輸入檔案名稱（input file）為 FILE|
|of=FILE|指定輸出檔案名稱（output file）為 FILE|
|count=N|只處理 N 個輸入區塊，每個區塊的大小為 ibs|

### wc word count

### tr
|tr||
|:-:|:-:|
|-c|用字符串1中字符集的補集替換此字符集，要求字符集為ASCII|
|-d|刪除字符串1中所有輸入字符|
|-s|刪除所有重復出現字符序列，只保留第一個；即將重復出現字符串壓縮為一個字符串|
- 後綴<br>

|||
|:-:|:-:|
|[a-z]|小寫a-z|
|[A-Z]|大寫A-Z|
|[1-9]|數字1-9|
|[:alpha:]|大小寫a-z|
|[:digit:]|0-9|
|[:alnum:]|大小寫a-z + 0-9|

### sort 
|sort||
|:-:|:-:|
|-g|以數字排列|
|-k|以第幾列為基準|
|-r|reverse|
|--ignore-case|不考慮大小寫|

### uniq


### Nmap 區域網路蒐尋器

### Netcat(nc)網路管理者工具

### alias
指令縮短
* 特殊用法:\(暫時取消)

### echo
"":內容
'':title