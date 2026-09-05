# Uranisys — WhatsApp 落地頁

`index.html` 是給 WhatsApp Business 個人檔案「網站」欄位用的落地頁。
客戶點連結 → 看到症狀牆與 30 秒自我檢核 → 直接用 WhatsApp 找我們。

## 上線前必做：填入 WhatsApp 號碼

打開 `index.html`，找到這一行（約在 581 行）：

    const WA_NUMBER = "__WA_NUMBER__";

改成國碼 + 號碼，不含 `+`、空格或 `-`。馬來西亞 012-345 6789 就寫：

    const WA_NUMBER = "60123456789";

全站三個 WhatsApp 按鈕與自我檢核結果的連結都吃這一個變數，改一次就好。

## WhatsApp 入口有四個

| 位置 | 帶入的訊息 |
|---|---|
| 主視覺按鈕「WhatsApp 直接聊聊」 | 想預約一次診斷 |
| 右下角浮動按鈕（全頁跟隨） | 想了解更多 |
| 頁尾 CTA「用 WhatsApp 預約診斷」 | 想預約一次診斷 |
| 自我檢核結果「把這個結果傳給我們」 | 自動帶入勾選項數與建議層次（L1–L4） |

最後一個最有用：客戶送出訊息時，你已經知道他卡在哪一層。

## 部署到 GitHub Pages

還沒推。要推的時候：

    gh repo create llffhh.github.io --public --source=. --push
    gh api -X POST repos/llffhh/llffhh.github.io/pages -f source[branch]=main -f source[path]=/

網址會是 `https://llffhh.github.io/`。上線後記得回頭補 `<head>` 裡的
canonical / og:url / og:image（og:image 是 WhatsApp 分享時的預覽圖，1200×630）。

## 檔案

- `index.html` — 落地頁（由 `bd-onepager-lite.html` 加上 WhatsApp 功能而來）
- `bd-onepager-lite.html` — 原始檔，未納入版控，保留作對照
