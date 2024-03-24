# Laravel 11 自動為應用程式套用程式碼風格

引入 tightenco 的 duster 套件來擴增自動為應用程式套用程式碼風格，協助檢查出各種語法相關的問題。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 你可以使用 `./vendor/bin/duster lint` 指令來檢查程式碼規範。
```sh
$ ./vendor/bin/duster lint
```

----

## 畫面截圖
![](https://i.imgur.com/RKUqYCk.png)
> 檢測出不符合程式碼規範的程式碼
