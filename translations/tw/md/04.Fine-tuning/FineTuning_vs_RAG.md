## 微調與RAG

## 檢索增強生成

RAG 是資料檢索加上文本生成。企業的結構化資料和非結構化資料儲存在向量資料庫中。當搜尋相關內容時，會找到相關摘要和內容形成上下文，並結合LLM/SLM的文本補全能力來生成內容。

## RAG 流程
![FinetuningvsRAG](../../../../translated_images/rag.20124d5657be35073dd1dbc93411c24ed912cbcc3bab5d37d28e648e6f175b7e.tw.png)

## 微調
微調是基於某個模型的改進。不需要從模型算法開始，但需要不斷積累數據。如果你在行業應用中需要更精確的術語和語言表達，微調是你的最佳選擇。但如果你的數據經常變動，微調會變得複雜。

## 如何選擇
如果我們的答案需要引入外部數據，RAG 是最佳選擇

如果你需要輸出穩定且精確的行業知識，微調會是一個好的選擇。RAG 優先拉取相關內容，但可能無法總是掌握專業的細微差異。

微調需要高品質的數據集，如果只是小範圍的數據，效果不會有太大差別。RAG 更靈活
微調是一個黑盒子，一種玄學，內部機制難以理解。但 RAG 可以更容易找到數據來源，從而有效調整幻覺或內容錯誤，提供更好的透明度。

免責聲明：本翻譯內容由AI模型從原文翻譯而來，可能不夠完美。請審核輸出結果並進行必要的修正。