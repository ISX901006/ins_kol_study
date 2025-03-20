# ins_kol_study

## 資料獲取
以使用DrissionPage抓取

Post佔全體貼文的58%
去除影片的內容後，貼文共24419篇

其中業配文共8880篇，約佔貼文總數的38%。

## 資料預處理
將文章按照post_id(ex: isx_o6_99)排序
去除IQR外的outlier後，抓取高的前30%，低的數據30%的文章

- 文章內容將去除/n
- cooperator & product_links：有值 → 1，沒值 → 0
- mentions_count：計算 @ 出現次數，空值補 0
- hashtags_count：計算 # 出現次數，空值補 0
- words_count：去掉空格後計算 article 欄位內的總字數（中英混雜）
