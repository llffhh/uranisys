# Uranisys — 公司介紹頁

`index.html` 是 `bd-onepager-lite.html` 的原樣複本（未修改），
給 WhatsApp Business 個人檔案的「網站」欄位使用。

網址：https://llffhh.github.io/uranisys/

## 更新內容

改 `bd-onepager-lite.html` 之後，複製過去再推上去：

    cp bd-onepager-lite.html index.html
    git add index.html && git commit -m "Update page" && git push

## 之後換成自有網域

1. 在這個資料夾建立 `CNAME`，內容寫網域，例如 `uranisys.com`
2. DNS 加 CNAME 記錄指向 `llffhh.github.io`
3. 推上去後到 repo Settings → Pages 勾選 Enforce HTTPS
4. 舊網址會自動轉址到新網域，WhatsApp 上的連結不會斷

## 名片 QR 網址（重要）

名片上的 QR code 指向 `/bd`，它會自動轉到 `/BD_page/`。

日後若改用 WordPress 或其他平台重做官網，**必須在新平台上重建 `/bd`**
（建立一個網址為 `bd` 的頁面，或設一個轉址），否則已印出的名片會失效。

## 名片 QR 網址（重要）

名片上的 QR code 指向 `/bd`，會自動轉到 `/BD_page/`。

日後若改用 WordPress 或其他平台重做官網，**必須在新平台重建 `/bd`**
（建立一個網址為 bd 的頁面，或設一個轉址），否則已印出的名片會失效。

首頁 `/` 目前也是轉址到 `/BD_page/`，等正式官網做好後再取代。
