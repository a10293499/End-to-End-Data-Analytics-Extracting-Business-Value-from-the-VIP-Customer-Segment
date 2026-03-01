# End-to-End-Data-Analytics-Extracting-Business-Value-from-the-VIP-Customer-Segment
#  從數據清理到商業決策：零售業 VIP 客戶價值分析專案
## Superstore Business analysis with SQLite and Power BI
 * Data 資料 
    * Name 資料名稱:大型賣場銷售資料集 (Superstore Dataset) 
    * Data Source 資料來源:<[Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)> 
 * Aim 目標
    * 使用SQLite和Power BI 對銷售資料進行趨勢分析、銷額獲利分析與VIP客戶分析

 * Methods方法
    * 使用ODBC連接SQLite和Power BI
    * 使用SQLite抓取資料
    > - [趨勢 SQLite code]()
    > - [商品類別與獲利]()
    > - [VIP客戶：前20%銷額]()
    > - [VIP客戶購買之商品類別]()
    > 
    * 使用Power BI繪製[動態圖表]()

 * Result 結果


   ![1](https://github.com/a10293499/End-to-End-Data-Analytics-Extracting-Business-Value-from-the-VIP-Customer-Segment/blob/main/1.%E5%B9%B4%E5%BA%A6%E9%8A%B7%E5%94%AE%E5%A2%9E%E9%95%B7%EF%BC%9A%E6%A5%AD%E7%B8%BE%E8%B6%A8%E5%8B%A2%E8%88%87%E5%AD%A3%E7%AF%80%E6%80%A7%E6%B3%A2%E5%8B%95%E5%88%86%E6%9E%90.png)
>圖1.2014-2017 銷售趨勢分析：Q4 季節性效應帶動業績高峰
>Figure1.Sales Trends 2014-2017: Seasonal Peaks in Q4
>
>
>2015到2017的銷額逐漸增加，尤其2015到2016年有大幅度增加22.8%。
以季度的角度分析，Q4為主要銷額來源，其中又以11月最為重要。觀察2017年的11月會發現在科技類產品與其他年度拉開差距，再細看次類別手機與影印機影響較大。
此外，2016年反而是在Q4的12月有更好的表現，主要由於家具類與其他產品類的拉抬，家具中的桌子與辦公用品類的活頁夾在此時表現優異。

-----------------


   ![2](https://github.com/a10293499/End-to-End-Data-Analytics-Extracting-Business-Value-from-the-VIP-Customer-Segment/blob/main/2.%E7%8D%B2%E5%88%A9%E5%93%81%E8%B3%AA%E7%9F%A9%E9%99%A3%EF%BC%9A%E7%94%A2%E5%93%81%E6%90%8D%E7%9B%8A%E8%A9%95%E4%BC%B0%E8%88%87%E7%B5%90%E6%A7%8B%E5%84%AA%E5%8C%96.png)
>圖2.獲利品質矩陣：產品損益評估與結構優化
>Figure2.Profitability Matrix: High-Margin Insights & Loss Optimization
>
>利潤高低的類別依序為科技類、辦公用品類與家具類。與銷額相比，家具類的利潤明顯較差，只占整體利潤的6.44%，且明顯低於另外兩者。
透過獲利象限分析發現，右上角是銷額跟利潤都高的產品，如科技類：電話、影印機、Accessories，家具類：椅子，辦公用品類：資料夾、Storage。左上角的Paper和Appliances，這類高槓桿產品，這雖然銷額看似低，但利潤高，可嘗試多推廣顧客購買此類產品。
右下角則是處於「高銷售、低獲利」的警示區，如桌子和Machines，可重新檢視其成本結構或調整定價策略。
左下角則是銷額與利潤都不好，若要更替銷售的產品可優先考量此區，尤其像是Supplies、Fasteners...等，銷售的數量也相對少，表示較難吸引客人訪店。

-----------------


   ![3](https://github.com/a10293499/End-to-End-Data-Analytics-Extracting-Business-Value-from-the-VIP-Customer-Segment/blob/main/3.%E6%A0%B8%E5%BF%83%E5%AE%A2%E6%88%B6%E5%83%B9%E5%80%BC%E9%91%91%E5%AE%9A%EF%BC%9AVIP%20%E8%B2%A2%E7%8D%BB%E5%BA%A6%E8%88%87%E5%8D%80%E5%9F%9F%E5%88%86%E4%BD%88.png)
>圖3.20% 核心客戶價值鑑定：VIP 貢獻度與區域分佈
>Figure3.VIP Identification: Revenue Contribution & Geographic Distribution
>
>為了優化整體的獲利結構，接下來我們將針對貢獻度最高的 VIP 客群進行深入剖析，本區視銷額花費佔前20%的顧客為VIP顧客，這些顧客總銷額花費USD1,106,064.33，佔總額的48% (USD2,297,200.86)。
分析這些VIP顧客的來源，主要是位於美國的西岸(31.45%)，尤其是Califorina為最大宗；其次則是東岸(28.3%)，像是New York、Pennsylvania、Washington，建議行銷預算應優先投放在西岸與東岸地區，以維持核心營收

-----------------

   ![4](https://github.com/a10293499/End-to-End-Data-Analytics-Extracting-Business-Value-from-the-VIP-Customer-Segment/blob/main/4.%E7%B5%90%E6%A7%8B%E6%B4%9E%E5%AF%9F%EF%BC%9A%E9%AB%98%E7%A7%91%E6%8A%80%E7%94%A2%E5%93%81%E7%82%BA%20VIP%20%E6%8E%A1%E8%B3%BC%E9%87%8D%E5%BF%83.png)
>圖4.VIP 消費行為深度分析：科技類產品採購偏好
>Figure4.Sales Trends 2014-2017: Seasonal Peaks in Q4
>
>VIP顧客消費的主要類別第一同樣為科技類，其次則為辦公用品類，最後才是家具類，利潤的順序與銷額順序相同。
分析散佈圖，右上角是銷額跟利潤都高的產品，如科技類：電話、影印機，家具類：椅子，辦公用品類：資料夾、Storage。左上角
右下角為警示區，如Machines和Table，雖然前者的銷額高但利潤低，且整體賣的數量少(P2左下)，建議可優化其成本結構，或將資源轉向高毛利產品（如 Copiers、Binders），然而有時大項產品是為了引流。像是桌子雖然利潤低，但賣的數量較多。
   
