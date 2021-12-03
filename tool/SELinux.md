## SELinux 
在多次上課中，我們都使用getenforce指令希望得出Disable，我不得其解，因此我查詢了getenforce的用途及嘗試了解為什摸需要修改etc/SELinux/config讓SELinux關閉
### SELinux 介紹
安全增強型 Linux（Security-Enhanced Linux）簡稱 SELinux，它是一個 Linux 內核模塊，也是 Linux 的一個安全子系統。<br>
SELinux 的結構及配置非常複雜，而且有大量概念性的東西，要學精難度較大。很多 Linux 系統管理員嫌麻煩都把 SELinux 關閉了。<br>
### SELinux 的作用
SELinux 主要作用就是最大限度地減小系統中服務進程可訪問的資源（最小權限原則）。<br>
設想一下，如果一個以 root 身份運行的網絡服務存在 0day 漏洞，黑客就可以利用這個漏洞，以 root 的身份在您的伺服器上為所欲為了。是不是很可怕？<br>
SELinux 就是來解決這個問題的。<br>
### DAC
在沒有使用 SELinux 的作業系統中，決定一個資源是否能被訪問的因素是：某個資源是否擁有對應用戶的權限（讀、寫、執行）。<br>
只要訪問這個資源的進程符合以上的條件就可以被訪問。<br>
而最致命問題是，root 用戶不受任何管制，系統上任何資源都可以無限制地訪問。<br>
這種權限管理機制的主體是用戶，也稱為自主訪問控制（DAC）。<br>
### MAC
在使用了 SELinux 的作業系統中，決定一個資源是否能被訪問的因素除了上述因素之外，還需要判斷每一類進程是否擁有對某一類資源的訪問權限。<br>
這樣一來，即使進程是以 root 身份運行的，也需要判斷這個進程的類型以及允許訪問的資源類型才能決定是否允許訪問某個資源。進程的活動空間也可以被壓縮到最小。<br>
即使是以 root 身份運行的服務進程，一般也只能訪問到它所需要的資源。即使程序出了漏洞，影響範圍也只有在其允許訪問的資源範圍內。安全性大大增加。<br>
這種權限管理機制的主體是進程，也稱為*強制訪問控制（MAC）*

### SELinux 基本概念
1. 主體（Subject）
2. 對象（Object）
3. 政策和規則（Policy & Rule）
4. 安全上下文（Security Context）
5. SELinux 的工作模式
6. SELinux 工作流程


### SELinux 基本操作
1. 模式
```centos
#　getenforce
```
SELinux 共有三種模式
* **Enforcing**：強制模式，依據設定來限制檔案資源存取。
* **Permissive**：寬容模式，不限制檔案資源存取，但仍會依據設定檢查並記錄相關訊息。
* **Disabled**：停用模式，SELinux 已被停用。
2. 
3. 模式切換
```centos
# cat /etc/selinux/config
```
### SELinux 錯誤分析和解決



參考文章：<br>
https://kknews.cc/code/jmn3l56.html
https://dotblogs.com.tw/echo/2017/06/19/linux_selinux_mode
