# my little airport 歌詞地圖

一張由歌詞建立嘅 my little airport 香港地圖。

**→ [睇地圖](https://loegunn.github.io/mlageo/)**

> 非官方、非商業嘅個人 project。同 my little airport、其唱片公司及任何相關單位冇任何關係，未經授權，亦唔代表樂隊立場。

---

## 呢個係咩

my little airport 廿年嚟唱過好多地方 —— 有啲仲喺度，有啲已經冇咗，有啲搵極都搵唔到。呢個地圖將佢哋逐個標返出嚟，每一個點都註明咗係點樣考證出嚟。

單一 HTML 檔，冇 build step、冇後端、冇追蹤。落載咗就離線用得（除咗地圖底圖）。

## 點解會有

老實講，我唔係超級無敵粉絲 —— 佢哋喺我年度播放量排第三。

砌呢個地圖嘅原因好簡單：2026 年 12 月終於開 show，想喺去之前將啲歌入面嘅地方認真行一次。開始查之後先發現，原來有唔少地方已經唔喺度，有啲就算仲喺度都已經唔同咗。查落去就變成而家咁。

所以呢個唔係一個權威資料庫，係一個歌迷自己整理嘅嘢。有錯請話我知。

> ⚠️ 溫馨提示
>
> 呢個嘢純粹係返工偷偷地整、冇 IT 底嘅產物。寫錯咗或者跑版嘅話，大家細力啲屌 🥹
> 有咩意見隨時同我講，希望大家玩得開心！

## 一條原則

**唔肯定，就唔假裝肯定。**

落得到區就落區，落唔到就唔落。唔會為咗個地圖好睇而砌一個點出嚟。

所以地圖上有五種唔同嘅點，各自代表唔同級別嘅證據：

| | |
|---|---|
| ● 歌詞地點・準確位置 | 歌詞講明，而且考證到實際位置 |
| ◦ 歌詞地點・地區代表點 | 知道係邊一區，但落唔到確實位置。個點只係話你知大概喺邊，唔等於歌講嗰個地方 |
| ◆ mla 聖地 | 唔係歌詞講嘅地點，係樂隊本身嘅地方。同歌詞地點分開，因為證據級別唔同 |
| ○ 已消失 | 歌入面嗰個地方而家已經唔喺度 |
| ⟋ 已變質 | 地方仲喺度，但同歌講嗰陣已經唔同咗 |

仲有「未解之地」—— 歌詞有名有姓講過、但考證唔到位置嘅地方。佢哋唔喺地圖上，但照樣列出嚟。**唔確定本身都係資料。**

App 入面「考證方法」一頁有完整說明同即時統計。

## 資料點嚟

- **歌詞**以官方發佈版本為準
- **地點考證**靠網上公開資料查證：官方網站、新聞報道、政府地政資料、維基百科、地圖服務
- **部分地點由朋友實地考察**核對過現況
- **少量判斷純粹係本地認知**（即係「我一直知道講緊嗰間」），呢類一定會喺 `note` 欄寫明，唔會扮成有實證

每個點嘅 `note` 都寫低咗依據，包括邊啲係實證、邊啲係推論。你可以自己判斷信唔信。

## 資料結構

資料層直接寫喺 `index.html` 入面：

| | 內容 |
|---|---|
| `SONGS` | 有地方掛住嘅歌 |
| `PLACES` | 地圖上嘅點。`precision` 分準確位置同地區代表點，`status` 記已消失／已變質 |
| `REFS` | 邊首歌講邊個地方。`line` 欄係歌詞證據，留空代表冇直接歌詞證據，UI 就唔會顯示 |
| `UNMAPPED` | 歌詞提過、有實地線索、但未確認位置 |
| `COVERAGE` | 覆蓋率：核過幾多首、收咗幾多、篩走幾多 |

逐首曲目嘅核實記錄（包括篩走嗰批嘅理由）喺另一個未公開嘅 workbook。

## 如果你想去行

地圖上好多地方係民居、街市、食肆、屋邨。麻煩：

- 尊重當地居民同商戶，唔好阻住人做生意
- 唔好擅闖私人地方
- 「地區代表點」唔係實際地址，唔好照住個坐標去撳人哋門鐘
- 有啲地方已經拆咗或者變咗，去到見唔到係正常

呢個地圖負責故事同考證，導航同實際路況請用 Google 地圖。

## 私隱

冇 analytics、冇 cookie、冇追蹤、冇收集任何資料。個網站只係一個靜態 HTML 檔。地圖底圖由 CARTO 提供，載入圖磚時你嘅瀏覽器會連去佢哋伺服器 —— 呢部分受 CARTO 同 OpenStreetMap 嘅政策規範。

## 版權

- 地圖介面同考證整理係個人研究成果，未授予任何開源授權
- 歌詞版權歸 my little airport 及原出版方所有。本站只引用短句作地理考證用途，每句均標明歌名、專輯及年份，唔提供完整歌詞，亦唔提供任何歌詞下載
- 引用旨在符合《版權條例》（第 528 章）第 39 條「批評、評論、引用及報道和評論時事」嘅公平處理豁免：作品已公開發行、引用程度唔大於考證所需、附有確認聲明
- 底圖 © OpenStreetMap contributors, © CARTO
- 相關商標、名稱歸各自持有人所有

如果你引用本站嘅資料，請註明出處：

> MLA Map by Loegunn — https://loegunn.github.io/mlageo/

---

## Copyright & Usage

This is an unofficial geographical map created out of a love for my little airport's music, compiled during urban wanderings and moments of listening. MLA Map documents not just locations, but footnotes of where these melodies once echoed across the city.

The original source code, interface design, original documentation, data organization, map presentation, and other original materials created by Loegunn are protected by applicable copyright law. **No open-source license is granted to this project at this time.**

You may view and use the publicly available MLA Map website for personal, non-commercial purposes.

Without prior permission, you may not:

- redistribute this project or substantial portions of it;
- republish the project as your own;
- present the project or substantial portions of it as your own work;
- create and redistribute a substantially similar copy of the project;
- remove or obscure the copyright notice.

If you reference or use substantial material from this project, please provide clear attribution:

> MLA Map by Loegunn — https://loegunn.github.io/mlageo/

Because these memories tied to locations are the most private dialogue between my little airport and this city.

### Disclaimer

This is an unofficial, fan-made project. It is not affiliated with, endorsed by, or officially connected to my little airport. my little airport and its related music, lyrics, names, trademarks, and other rights belong to their respective rights holders.

Lyrics are quoted only in short fragments for the purpose of geographical research, with the song title, album and year always attributed. No complete lyrics are reproduced or made available for download.

Basemap © OpenStreetMap contributors, © CARTO.

## 有問題請聯絡

如果你係版權持有人、地點業主、或者任何覺得本站內容侵犯咗你權益嘅人 —— **請開一個 [issue](https://github.com/loegunn/mlageo/issues) 話我知，我會即時移除相關內容，唔會爭辯。**

同樣，如果發現考證錯誤、或者知道緊「未解之地」邊個地方喺邊，都歡迎開 issue。

## 免責

本站按現狀（as is）提供，唔作任何明示或暗示嘅保證。

所有考證都可能有錯，部分內容明確屬於推論。請勿當作權威資料引用，亦請勿單靠本站資料作任何決定。作者唔會就使用本站資料而引致嘅任何損失承擔責任。

本站純屬個人興趣，非商業、冇收益、冇廣告。

## 技術

單一 HTML 檔，Leaflet + CARTO 底圖，冇框架冇 build。

網址支援深層連結：`#place=` `#song=` `#view=gone` `#view=unmapped` `#view=method` `#q=` `#mode=songs` `#region=world`

寬過 820px 出 sidebar + 地圖，窄過變全屏地圖 + 底部 sheet。同一份 code。

## 狀態

持續整理中。
