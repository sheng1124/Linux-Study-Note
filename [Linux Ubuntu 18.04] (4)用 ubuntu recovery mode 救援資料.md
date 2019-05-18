# [Linux Ubuntu 18.04] (4)用 ubuntu recovery mode 救援資料
## 當 Ubuntu 無法正常開機時，需要重灌時，又忘了備份
### 1. 取得 Recovery mode 可寫入的權限，並進入檔案系統
* 開機 ubuntu 圖案 按 esc
* 進入 grub 選單
* 方向鍵選到 xxx(recovery mode)
* 按 e 編輯
* 將 ro recovery nomodeset 改為 rw  recovery nomodeset 
* 按 ctrl+x或者F10 進入如下界面，輸入密碼即可
    ![](https://i.imgur.com/hdiEQHW.png)

### 2. 掛載 USB
* ```fdisk -l``` 查詢當前系統可讀到的硬體儲存設備
    ```linux=
    # fdisk -l
    ```
    * 我的 device 為 sda1
    ![](https://i.imgur.com/tlHKEoz.png)

* 執行 ```mount``` 指令
    ```linux=
    # mkdir /mnt/usb
    # mount dev/sda1 /mnt/usb
    ```
    ![](https://i.imgur.com/yVNAJaB.png)

### 3. 備份資料
* 掛載好 USB 即可存取 USB
* 可移動路徑至想要的位置，如果檔案沒壞，資料都是完整的
    ```linux=
    # cd /home/shengfu
    ```
* 可用 ls -a 檢視隱藏資料
* cp 資料 到 USB
* umount USB
    ```linux=
    # umount dev/sda1
    ```
### 參考資料
* ubuntu进入recovery mode修改系统文件
    * http://www.xitongjiaocheng.com/ubuntu/2018/63894.html
* 掛載 USB
    * http://learn-garden.blogspot.com/2008/08/linuxu.html
 ###### tags: `Linux`