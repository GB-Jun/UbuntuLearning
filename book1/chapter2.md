# 系統安裝介紹
## 安裝前的準備
### 安裝媒介的選擇
光碟，網路安裝，USB
### 主機的硬體需求

## 桌面系統安裝
### 安裝過程導覽
書中使用光碟說明
> Linux 系統中root是權限最高的帳號，但ubuntu在安裝時並沒有設定密碼，而在系統安裝流程時會有新增一個一般帳號但其實此時新增的帳號有包含root的權限，故其帳密必須特別注意
### root 密碼設定與遠端連線
root 設定密碼
    使用terminal
    sudo passwd root
單純切換root身分
    sodu su -
安裝vim
    apt-get install vim
安裝openssh
    apt-get install opssh-server
使用root連線ssh伺服器需更改設定
    修改設定檔 /etc/ssh/sshd_config
    修改為PermitRootLogin yes
    修改後執行 systemctl restart sshd.service
## USB啟動介紹
### 製作USB啟動碟
使用win32 Imager，依照安裝引導安裝，開啟時須使用管理者權限，開啟軟體後依照畫面UI所需選擇映像檔和USB磁碟，按下yes後等待製作完成
### USB啟動碟介面介紹
插入USB後才開機，用esc、F2或F10進入BIOS設定開機順序使用USB開機，或是F8進入開機選單選擇USB開機，之後即可以選擇安裝或試用utunbu