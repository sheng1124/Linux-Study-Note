# [Linux Ubuntu 18.04] (0) Linux 常用指令

## 檔案管理
### 移動
```Linux=
cd /path
```
```Linux=
cd ~/path
```
* 移到家目錄
```Linux=
cd ~
```
### 檢視檔案
```Linux=
ls 
```
* 顯示隱藏檔
```Linux=
ls -a
```

### 目錄管理

* 建立目錄
    ```Linux=
    rm -r directories
    ```

* 刪除目錄
    ```Linux=
    rm -r directories
    ```
*  yes 自動回答一堆 rm 的 question
    ```Linux=
    $ yes | rm -r directories
    ```
### 刪除資料
### 工作管理
* 顯示當前 terminal 下的工作
    ```linux=
    $ jobs
    ```
* 結束工作
    ```linux=
    $ kill %1
    ```
* 把命令放到背景執行
    ```linux=
    $ 指令 &
    ```
* 把工作帶回前景
    ```linux=
    $ fg %1
    ```
    ```linux=
    $ fg 8521
    ```
    * 8521=>pid
* 暫停程序
    * ctrl + z
* 希望暫停的程序能繼續在背景中執行
    ```linux=
    $ bg %1
    ```
### 腳本製作
* 修改腳本屬性
    ```linux=
    $ chmod a+x hello.sh
    ```
* 執行腳本
    ```linux=
    $ ./hello.sh
    ```

###### tags: `Linux`