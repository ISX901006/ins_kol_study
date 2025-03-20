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

colab抓地端資料先跑，bigqurey
圖文都轉成數值特徵了
特徵工程先不用

要有多個特徵組合(網紅特徵、圖片、文字，)
找模型開始倒進去

是要找到準確性高，還是要探討特徵對y的影響性

文章少了bertopic

gemini物件偵測的集合大概有多少個

目前有文章特徵、圖片特徵、網紅特徵、產品類別
全因子實驗設計*各種模型


