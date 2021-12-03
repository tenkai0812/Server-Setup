## install
### 系統對應安裝套件
|系統|安裝套件|
|:-:|:-:|
|CENTOS|yum|
|FEDORA|yum|
|REDHAT|yum|
|UBUNTU|apt-get|
### 安裝rpm套件準備動作
- 系統管理員權限
- 網路下載或光碟機取得rpm檔案
- 利用rpm安裝指令
### rpm function

|rpm |||
|:-:|:-:|:-:|
|-i|install||
|-e|erase|刪除套件|
|-v|verbose||
|-h|has進度條||
|-U|upgrade||
|-q|query|僅查詢，後面接的套件名稱是否有安裝|
|-qa|query all|列出所有已經安裝在本機 Linux 系統上面的套件名稱|
|-qi|query information|列出該套件的詳細資訊，包含開發商、版本與說明等|
|-ql|query list|列出該套件所有的檔案與目錄所在完整檔名|
|-qf|query found|由後面接的檔案完整名稱，找出該檔案屬於哪一個已安裝的套件|
|--nodeps|||
|--force|||
### rpm 套件種類
|平台名稱|適合平台說明|
|:-:|:-:|
|i386|幾乎適用於所有的 x86 平台，不論是舊的 Pentium 或者是新的 Intel Core 2 與 K8 系列的 CPU 等等，都可以正常的工作！那個 i 指的是 Intel 相容的 CPU 的意思，至於 386 不用說，就是 CPU 的等級啦！|
|i586|就是針對 586 等級的電腦進行最佳化編譯。那是哪些 CPU 呢？包括 Pentium 第一代 MMX CPU， AMD 的 K5, K6 系列 CPU (socket 7 插腳) 等等的 CPU 都算是這個等級；|
|i686|在 Pentium II 以後的 Intel 系列 CPU ，及 K7 以後等級的 CPU 都屬於這個 686 等級！ 由於目前市面上幾乎僅剩 P-II 以後等級的硬體平台，因此很多 distributions 都直接釋出這種等級的 RPM 檔案。|
|x86_64|針對 64 位元的 CPU 進行最佳化編譯設定，包括 Intel 的 Core 2 以上等級 CPU ，以及 AMD 的 Athlon64 以後等級的 CPU ，都屬於這一類型的硬體平台。|
|noarch|就是沒有任何硬體等級上的限制。一般來說，這種類型的 RPM 檔案，裡面應該沒有 binary program 存在， 較常出現的就是屬於 shell script 方面的軟體。|
### rpm 麻煩點
rpm若software建立在lib A 跟 lib B，且lib A又建立在lib C上，rpm安裝順序為lib C >lib A >lib B >software。否則會出錯。因為麻煩，所以出現了yum
### yum 
- 解決套件之間相依性與版本複雜性
- 
- 
- 
### yum function

|yum||
|:-:|:-:|
|install|下載|
|update|更新|
|remove|移除|
|groupinstall|群體下載|
|search|查詢|

### nfs


