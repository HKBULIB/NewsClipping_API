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
 

## Query Parameters
The following examples show how to use different query parameters to output data of specific issues from the dataset.

**Example 1**: Results returned by specific record ID number (NCA-003074):

https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?id=NCA-003074
```
{
    "totalResults": 1,
    "Results": [
        {
            "id": "NCA-003074",
            "title": "重慶園杏同春班",
            "type": "廣告",
            "newspaper": "華字日報",
            "author": null,
            "publishedLocation": "香港",
            "publishedDate": "1900-02-23",
            "language": "繁體中文",
            "collection": "film",
            "mediaMention": [
                "奇巧洋畫"
            ],
            "peopleMention": null,
            "unitMention": [
                "杏同春班",
                "重慶園"
            ],
            "abstract": "重慶園換新粵劇戲碼，加演奇巧洋畫",
            "keywords": [
                "華文報紙電影史料",
                "電影廣告"
            ],
            "url": "https:\/\/digital.lib.hkbu.edu.hk\/newsclipping\/record.php?ids=NCA-003074",
            "scan_url": null
        }
    ]
}
```

**Example 2**: Results returned by specific starting year:

https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?startYear=1954
```
{
    "totalResults": 33186,
    "Results": [
        {
            "id": "NCB-000022",
            "title": "傳教士林樂知、李提摩太的思想，帝國主義奴役殖民地人民的工具",
            "type": "新聞及文章",
            "newspaper": "光明日報",
            "author": "馮友蘭",
            "publishedLocation": "北京",
            "publishedDate": "1954-05-19",
            "language": "繁體中文",
            "collection": "religion",
            "mediaMention": null,
            "peopleMention": [
                "Allen, Young John, 1836-1907",
                "Richard, Timothy, 1845-1919"
            ],
            "unitMention": null,
            "abstract": null,
            "keywords": [
                "天主教與基督教",
                "組織條例與指示言論"
            ],
            "url": "https:\/\/digital.lib.hkbu.edu.hk\/newsclipping\/record.php?ids=NCB-000022",
            "scan_url": "https:\/\/storage.lib.hkbu.edu.hk\/projects\/newsclipping\/religion\/er00047m.pdf"
        },
        ...
        ...
    ]
}
```

**Example 3**: Results returned by a specific collection (overseas, religion, or films):

https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?collection=overseas
```
{
    "totalResults": 33765,
    "Results": [
        {
            "id": "NCC-000001",
            "title": "利用華僑力量，經濟封鎖中共，國府設專責機構",
            "type": "新聞及文章",
            "newspaper": "自然日報",
            "author": null,
            "publishedLocation": "香港",
            "publishedDate": "1952-10-20",
            "language": "繁體中文",
            "collection": "overseas",
            "mediaMention": null,
            "peopleMention": null,
            "unitMention": null,
            "abstract": null,
            "keywords": [
                "臺灣",
                "僑務機構"
            ],
            "url": "https:\/\/digital.lib.hkbu.edu.hk\/newsclipping\/record.php?ids=NCC-000001",
            "scan_url": "https:\/\/storage.lib.hkbu.edu.hk\/projects\/newsclipping\/overseas\/00000008.pdf"
        },
        ...
        ...
    ]
}
```






### Output Limit
Note that each API query only returns a JSON result of 20 articles. To return more issues, use *limit* parameter
```
https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?start=0&limit=300


```

Using a combination of *limit* and *start* parameters, one can also applies pagniation when scraping the dataset:
```
https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?start=0&limit=10
https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?start=11&limit=10
https://digital.lib.hkbu.edu.hk/api/chinese_newsclipping/?start=21&limit=10
```

## License
CC BY-NC
https://creativecommons.org/licenses/by-nc/4.0/

![](https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc.png)


