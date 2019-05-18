# [Linux Ubuntu 18.04] (3) 實作腳本 script
## 變數的取用
* echo
    * 利用 echo 這個指令來取用變數，但是，變數在被取用時，前面必須要加上錢字號『 $ 』才行
    * 利用 echo 就能夠讀出，或者是以 ${變數} 的方式來取用都可以
    ```linux=
    $ echo $variable
    $ echo $PATH
    $ echo ${PATH}  # 近年來，鳥哥比較偏向使用這種格式喔！
    ```
* 『設定』或者是『修改』 某個變數的內容
    * 用『等號(=)』連接變數與他的內容
    ```linux=
    $ myname=${VBird}
    ```
* 變數的設定規則
    * 等號兩邊不能直接接空白字元
    * 變數名稱只能是英文字母與數字，但是開頭字元不能是數字
    * 通常大寫字元為系統預設變數，自行設定變數可以使用小寫字元，方便判斷
    * 若該變數需要在其他子程序執行，則需要以 export 來使變數變成環境變數
## 條件判斷式
* 參考網路
## 迴圈
* 參考網路
## 分割字串
* https://www.opencli.com/linux/shell-script-substring
## 範本
* rotate-princess
    * 旋轉螢幕的程式，釘選到工具欄，不靠輸入指令，快速旋轉螢幕，用 xrandr 實作
## 參考資料
* 鳥哥
    * http://linux.vbird.org/linux_basic/0320bash.php
    * http://linux.vbird.org/linux_basic/0340bashshell-scripts.php#some_ex
* Bash Scripting Tutorial
    * https://ryanstutorials.net/bash-scripting-tutorial/
* If / Else Statements (Shell Scripting)
    * http://codewiki.wikidot.com/shell-script:if-else 
* Shell Script 截取部份字串
    * https://www.opencli.com/linux/shell-script-substring
* [Shell Script] 簡單說明
    * https://blog.xuite.net/tolarku/blog/83050297-%5BShell+Script%5D+%E7%B0%A1%E5%96%AE%E8%AA%AA%E6%98%8E

###### tags: `Linux`