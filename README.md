# API for HKBU《華人剪報資料庫》(Chinese News Clipping Database)

## Background
《華人剪報資料庫》匯集由香港浸會大學圖書館從不同途徑收集而來的早期及現代與華人有關的報紙剪報。經過相關資料文本的整理及編索後，《華人剪報資料庫》所含的歷史資料數目龐大且珍貴，資料庫更提供電子檢索，不僅方便查閱，更超越地域限制，大大降低獲取原始資料的難度。

https://digital.lib.hkbu.edu.hk/newsclipping/index.php


## Resource URL
```
https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/
```

## API Outputs
 The API returns the following output (for each newsclipping entry):
 - article title (headline)
 - content type (news or advertisement)
 - author(s)
 - published location
 - published date
 - language (English, Simplified Chinese or Traditional Chinese)
 - collection (film, religion or overseas)
 - abstract
 - what media (films, TV program) were mentioned in the news clippping
 - persons mentioned in the news clipping
 - organization or units mentioned in the news clipping
 - list of keywords indexed from the contents
 - URL of the newsclipping record on 《華人剪報資料庫》(HKBU Library) 
 - URL of the newsclipping PDF scan on 《華人剪報資料庫》(HKBU Library) (if any)
 

## Sample Usage (Python)
