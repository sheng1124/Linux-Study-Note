# [Linux Ubuntu 18.04] (2) 使用腳本 script

## 使用者介面
* Shell
    * Shell 是一個與 kernel 溝通的軟體
    * 你必須要『輸入』一個指令之後， 『硬體』才會透過你下達的指令來工作！
    * 硬體如何知道你下達的指令呢？
        * 我們必須要透過『 Shell 』將我們輸入的指令與 Kernel 溝通
    ![](https://i.imgur.com/v68aAfZ.png)
* Shell 的版本
    * Bourne SHell
        * 第一個流行的 shell ，簡稱為 sh
    * C SHell
        * 這個 shell 的語法有點類似 C 語言，所以才得名為 C shell ，簡稱為 csh
    * Bash
        *  目前是 Linux distributions 的標準 shell，是 Bourne Shell 的增強版本，也是基準於 GNU 的架構下發展出來的
        * 支援 程式化腳本： (shell scripts)

## Shell scripts
*  shell script 是利用 shell 的功能所寫的一個『程式 (program)』
*  script 是『腳本、劇本』的意思。整句話是說， shell script 是針對 shell 所寫的『劇本！』
*  不用一行一行輸入指令，透過 shell script 幫我們完成工作
*  而且 shell script 更提供陣列、迴圈、條件與邏輯判斷等重要功能，讓使用者也可以直接以 shell 來撰寫程式，而不必使用類似 C 程式語言等傳統程式
*  shell script 可以簡單的被看成是批次檔， 也可以被說成是一個程式語言

## 建立 Shell script 
* 建立 123.sh 檔案 
* /home/123/123.sh 好了，那如何執行這個檔案？
    * 以 bash 程式來執行：透過『 bash 123.sh 』或『 sh 123.sh 』來執行
    * 直接指令下達， shell.sh 檔案必須要具備可讀與可執行 (rx) 的權限 ```chmod +x 123.sh```、執行: ```路徑/123.sh```
    ```linux=
    $ ./123.sh #'.'是當前路徑
    $ ~/123.sh #開啟家目錄底下的123.sh
    ```
    * 雙擊執行，必須要具備可讀與可執行 (rx) 的權限，且要設定資料夾選項，將可執行檔案設定成 run them ， files -> perference ->  Behavior -> Executable Text Files -> Run them
    ![](https://i.imgur.com/YRdrVp6.png)

## 新增自定義程式到應用程式清單中
* 在 ~/.local/share/applications 中創一個.desktop檔案
* 建立 123.desktop 檔案，內容為
    ```=
    [Desktop Entry]
    Encoding=UTF-8
    Version=1.0
    Type=Application
    Terminal=false
    Exec=/home/123/app/123.sh
    Name=123
    Icon=/home/123/app/123.png
    ```
    * Encoding 表示執行所用的編碼
    * Name在清單中會顯示的應用程式名稱
    * Exec為程式開啟的位置或指令
    * Icon為在清單中會顯示的圖示，如果應用程式本身沒有提供，可以自行選擇其他圖片
    * Terminal 為是否可以在terminal模式中開啟
* 設定好之後就可以在應用程式清單看到該程式
     ![](https://i.imgur.com/DP4xaMh.png)

## 參考資料
* 鳥哥
    * http://linux.vbird.org/linux_basic/0320bash.php
    * http://linux.vbird.org/linux_basic/0340bashshell-scripts.php#some_ex
* 如何在ubuntu新增自定義程式到應用程式清單中(Desktop Entry) 
    * https://xenby.com/b/167-%E6%95%99%E5%AD%B8-%E5%A6%82%E4%BD%95%E5%9C%A8ubuntu%E6%96%B0%E5%A2%9E%E8%87%AA%E5%AE%9A%E7%BE%A9%E7%A8%8B%E5%BC%8F%E5%88%B0%E6%87%89%E7%94%A8%E7%A8%8B%E5%BC%8F%E6%B8%85%E5%96%AE%E4%B8%ADdesktop-en
* How to Create a .Desktop File For Your Application in Linux
    * https://www.maketecheasier.com/create-desktop-file-linux/ 
* If / Else Statements (Shell Scripting)
    * http://codewiki.wikidot.com/shell-script:if-else
###### tags: `Linux`